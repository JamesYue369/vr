# 先上效果
[点击观看](https://jamesyue369.github.io/vr/)如果卡顿可以查看下面的效果页面截图<br/>
<img src="https://jamesyue369.github.io/vr/WX20230205-095113.png" />
<img src="https://jamesyue369.github.io/vr/WX20230205-095200.png" />
<img src="https://jamesyue369.github.io/vr/WX20230205-095228.png" />
如果还满意的话，客官打赏下吧，即可获取源码和小二的技术支持（请加VX）<br/>
<img src="https://jamesyue369.github.io/vr/WechatIMG268.jpeg" width="210px" height="300px"/>
<img src="https://jamesyue369.github.io/vr/WechatIMG267.jpeg" width="210px" height="300px"/>
# 版权声明
允许个人或公司进行二次开发，不允许二次售卖，否则追究法律责任！
# React 版本 VR看房插件
# 使用方法
`import Vr from 'vr';`
```
<div>
  <Vr data={这里是参数配置} />
</div>
```
# 参数说明
```
{
  axes: false,  // axes 是否开启坐标显示
  houses: [{   // houses 是房间配置
    type: 'main', // type 是房间类型 main代表是页面展示的第一个房间
    texture: 'keting.jpeg', // texture 是房间的3D全景贴图
    name: 'keting', //name 是房间的ID
    routes: [{ // routes 是当前房间内跳转其他房间的路由配置
      to: 'canting', // to 是要跳转的房间id 对应上面的name值
      label: '餐厅', // label 是跳转文本
      position: { // 显示跳转按钮在房间内的世界坐标位置
        x: -0.29,
        y: -0.34,
        z: -0.8
      }
    }]
  }, {
    type: 'normal',
    name: 'canting',
    texture: 'canting.jpeg',
    routes: [{
      to: 'keting',
      label: '客厅',
      position: {
        x: -0.62,
        y: -0.28,
        z: -0.61
      }
    }, {
      to: 'zhuwo',
      label: '主卧',
      position: {
        x: -0.67,
        y: -0.6,
        z: 0.39
      }
    }, {
      to: 'ciwo',
      label: '次卧',
      position: {
        x: -0.6,
        y: -0.56,
        z: 0.13
      }
    }]
  }, {
    type: 'normal',
    name: 'zhuwo',
    texture: 'zhuwo.jpeg',
    routes: [{
      to: 'canting',
      label: '餐厅',
      position: {
        x: -0.06,
        y: -0.45,
        z: -0.8
      }
    }]
  }, {
    type: 'normal',
    name: 'ciwo',
    texture: 'ciwo.jpeg',
    routes: [{
      to: 'canting',
      label: '餐厅',
      position: {
        x: -0.79,
        y: -0.55,
        z: 0.12
      }
    }]
  }]
}
```
