# qui-mask

> 弹层组件，可通过slot定制内容

## 预览

<img src="https://qapp-ui.github.io/qapp-ui/docs/assets/qui-mask.gif" width="300"/>

## 依赖接口

无依赖

## 使用方法
	
```ux
<import name="qui-mask" src="@qapp-ui/qui-mask/index"></import>

<template>
  <div class="page-doc">
    <input class="input-button" type="button" value="显示mask" onclick="showmask" />
    <qui-mask visible="{{visible}}" show-close="{{showClose}}" @qui-overlay-click="overlayClick" @qui-close-click="closeClick">
      <div class="mask">
        <text class="mask-title">快应用</text>
        <text class="mask-txt">快应用是一套以前端开发技术栈为主进行应用开发的框架，采用流行的前端开发模式，贴合主流前端开发者的思维习惯，同时大幅提升应用的性能，提供大量前端环境无法使用的系统能力，以及很多第三方服务的对接能力。</text>
      </div>
    </qui-mask>
  </div>
</template>

<script>
  export default {
    private: {
      visible: '0',
      showClose: '0'
    }
  }
</script>
```

更详细代码可以参考 [qui-mask demo](https://github.com/qapp-ui/qapp-ui/blob/master/src/Mask/index.ux)

### 参数

| 属性名 | 类型 | 是否必填 | 默认值 | 描述 |
|-------------|------------|--------|-----|-----|
| visible | `String` | `N` |`0`| 是否显示，`'1'`表示显示，`'0'`表示隐藏 |
| showClose | `String` |`N`| `1` | 是否显示关闭按钮，`'1'`表示显示，`'0'`表示不显示 |
| closeIcon | `String` |`N`| `base64格式图片` | 关闭按钮uri（默认采用base64格式） |
| background | `String` |`N`| `rgba(0,0,0,0.4)` | 蒙层背景色 |

### 事件

| 事件名 | 参数 | 描述 | 
|----------|-----|-----|
| qui-overlay-click | `-` | 蒙层点击事件 | 
| qui-close-click | `-` | 关闭按钮点击事件 | 


