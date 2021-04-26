<!--  -->
<template>
  <div class="Box">


    <BarChart style="height: 450px;  width: 450px;" :dataObj="dataObj.data1" ref="exampleTestItem"></BarChart>

    <PieChart style="height: 450px; width: 450px;" :dataObj="dataObj.data2" ref="examplePie"></PieChart>


  </div>
</template>

<script>
  //这里可以导入其他文件（比如：组件，工具js，第三方插件js，json文件，图片文件等等）
  //例如：import 《组件名称》 from '《组件路径》';
  import BarChart from "@/common/chart/barChart";
  import PieChart from "@/common/chart/pieChart";

  export default {
    //import引入的组件需要注入到对象中才能使用
    components: {
      BarChart,
      PieChart,
    },
    data() {
      //这里存放数据
      return {
        dataObj: {
          data1: {
            name: "杀伤力",
            color: ['#1890ff', '#2fc25b', '#facc14', '#223273', '#8543e0', '#13c2c2'],
            data: [{
                name: "AK47",
                value: 3000,
              },
              {
                name: "Mp5冲锋枪",
                value: 2500,
              },
              {
                name: "榴弹",
                value: 1000,
              },
              {
                name: "AWP狙击枪",
                value: 8000,
              },
              {
                name: "加农炮",
                value: 28000,
              },
              {
                name: "马克沁机枪",
                value: 12000,
              },
            ],
            mode: "horizontal",
          },
          data2: {
            title: "某次军事演习",
            color: [
              "#1890ff",
              "#facc14",
              "#2fc25b",
              "#13c2c2",
              "#f04864",
              "#8543e0",
            ],
            data: [{
                name: "空军1",
                value: 1000,
              },
              {
                name: "陆军",
                value: 1050,
              },
              {
                name: "海军",
                value: 2000,
              },
            ],
          },
        },
      };
    },
    //监听属性 类似于data概念
    computed: {},
    //监控data中的数据变化
    watch: {},
    //方法集合
    methods: {},
    //生命周期 - 创建完成（可以访问当前this实例）
    created() {},
    //生命周期 - 挂载完成（可以访问DOM元素）
    mounted() {},
    beforeCreate() {}, //生命周期 - 创建之前
    beforeMount() {}, //生命周期 - 挂载之前
    beforeUpdate() {}, //生命周期 - 更新之前
    updated() {}, //生命周期 - 更新之后
    beforeDestroy() {}, //生命周期 - 销毁之前
    destroyed() {}, //生命周期 - 销毁完成
    activated() {}, //如果页面有keep-alive缓存功能，这个函数会触发
  };

</script>
<style scoped>
</style>
