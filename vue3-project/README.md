## 项目介绍
    采购系统  

## 技术点
    Vue3 + Vue-router + Pinia + Element-plus + axios  

## 安装element-plus 
1. 安装命令
    npm install element-plus --save

2. 引入
    1. 全导入
    ```js
        import { createApp } from 'vue'
        import ElementPlus from 'element-plus'
        import 'element-plus/dist/index.css'
        import App from './App.vue'

        const app = createApp(App)

        app.use(ElementPlus)
        app.mount('#app')
    ```

    2. 按需引入
        1. 下载依赖包
            npm install -D unplugin-vue-components unplugin-auto-import
        2. 配置文件
            


## 安装依赖
1. vue vue-router 
2. npm i normalize.css 
3. npm i axios -S   / npm i querystring -S
4. npm i echarts -S 


## echarts
1. 安装
    npm i echarts -S

2. 按需引入
   ```js
        // 引入 echarts 核心模块，核心模块提供了 echarts 使用必须要的接口。
        import * as echarts from 'echarts/core';
        // 引入柱状图图表，图表后缀都为 Chart
        import { BarChart } from 'echarts/charts';
        // 引入提示框，标题，直角坐标系，数据集，内置数据转换器组件，组件后缀都为 Component
        import {
        TitleComponent,
        TooltipComponent,
        GridComponent,
        DatasetComponent,
        TransformComponent
        } from 'echarts/components';
        // 标签自动布局、全局过渡动画等特性
        import { LabelLayout, UniversalTransition } from 'echarts/features';
        // 引入 Canvas 渲染器，注意引入 CanvasRenderer 或者 SVGRenderer 是必须的一步
        import { CanvasRenderer } from 'echarts/renderers';

        // 注册必须的组件
        echarts.use([
        TitleComponent,
        TooltipComponent,
        GridComponent,
        DatasetComponent,
        TransformComponent,
        BarChart,
        LabelLayout,
        UniversalTransition,
        CanvasRenderer
        ]);

        // 接下来的使用就跟之前一样，初始化图表，设置配置项
        var myChart = echarts.init(document.getElementById('main'));
        myChart.setOption({
        // ...
        });
   ```

