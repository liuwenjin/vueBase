<template>
  <div>
    <LineChart
      style="height: 450px"
      :dataObj="dataObj"
      ref="exampleTestItem"
    ></LineChart>
  </div>
</template>
<script>
// import LineChart from "@/common/chart/lineChart";
export default {
  components: {
    LineChart: ()=> import("@/common/chart/customChart"),
  },
  mounted() {
    $.when(
      $.get('https://cdn.jsdelivr.net/gh/apache/echarts-website@asf-site/examples/data/asset/data/option-view.json')
    ).done(res => {
      this.dataObj = res
    })
  },
  data() {
    return {
      dataObj: {},
    };
  },
  methods: {
    updateData(data) {
      this.dataObj = data;
      this.$nextTick(function(){
        this.$refs.exampleTestItem.updateData(this.dataObj);
      });

    },
  },
};
</script>
<style scoped>
* {
  box-sizing: border-box;
}
</style>
