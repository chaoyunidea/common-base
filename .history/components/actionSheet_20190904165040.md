## 弹窗示例 {docsify-ignore-all}

**标签名:action-sheet**

**说明:用于创建可由返回键控制的弹窗**

parent.vue
```
  <Child :opened.sync="opened" ></Child>
```
child.vue
``` 
  <style lang="scss">
    .acsheert{
      @include position-absolute;
    }
    .wrap{
      background: #fff;
      .contianer{
        width:100%;
        height:44px;
        line-height: 44px;
        text-align: center;
      }
    }
  </style>
  
  <template>
      <action-sheet
          v-if="opened"
          :data="list"
          @close="close"
          class='acsheert'
      >
          <!-- content -->
          <div class="wrap">
            <div class='contianer' v-for="(i,index) of list" :key="index">{{index}}</div>
          </div>
      </action-sheet>
  </template>

  <script>
    export default {
      mixins: [app.mixin.popupWindowRouteMixin],//必须混入
      props: {
        opened: {
            type: Boolean,
            default: false
          }
        },
        data() {
          return {
            list:new Array(20)  //控制滚动刷新的数据
          };
        },
      };
  </script>

```


 
## 标签属性说明

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| data | 内容集合,动态列表时需要传入 | any | null  |
| scrollerConfig | 滚动配置 | Object | {                        tag:'base',     //base或load或super                        api:null,          //load和super的参数                        type:2,             //load和super的prop参数,加载和刷新的方式.                       pagingOption:{}     //load和super的prop参数                    }   |
| maskToClose | 是否点击遮罩层关闭 | Boolean | true |
| position | 内容弹出位置 | String |  取值范围'top','bottom','center', 'sideLift', 'sideRight'  |
| header | 头部标题| String |  |   
| footer | 底部文字 | String |   |
| scrollerStyle | 滚动栏样式 | Object |   |
| fullParent | 侧滑推出时是否填充满父容器 | Boolean | false  |
 
