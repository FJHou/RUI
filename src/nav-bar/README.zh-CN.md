# NavBar 导航栏

### 引入

``` javascript
import { NavBar } from 'vant';

Vue.use(NavBar);
```

## 代码演示

### 基础用法

```html
<van-nav-bar
  title="标题"
  left-text="返回"
  right-text="按钮"
  left-arrow
  @click-left="onClickLeft"
  @click-right="onClickRight"
/>
```

```js
export default {
  methods: {
    onClickLeft() {
      Toast('返回');
    },
    onClickRight() {
      Toast('按钮');
    }
  }
}
```

### 高级用法

通过插槽定制内容

```html
<van-nav-bar title="标题" left-text="返回" left-arrow>
  <van-icon name="search" slot="right" />
</van-nav-bar>
```

## API

### Props

| 参数 | 说明 | 类型 | 默认值 | 版本 |
|------|------|------|------|------|
| title | 标题 | `string` | `''` | - |
| left-text | 左侧文案 | `string` | `''` | - |
| right-text | 右侧文案 | `string` | `''` | - |
| left-arrow | 是否显示左侧箭头 | `boolean` | `false` | - |
| fixed | 是否固定在顶部 | `boolean` | `false` | - |
| border | 是否显示下边框 | `boolean` | `true` | - |
| z-index | 元素 z-index | `number` | `1` | - |

### Slots

| 名称 | 说明 |
|------|------|
| title | 自定义标题 |
| left | 自定义左侧区域内容 |
| right | 自定义右侧区域内容 |

### Events

| 事件名 | 说明 | 回调参数 |
|------|------|------|
| click-left | 点击左侧按钮时触发 | - |
| click-right | 点击右侧按钮时触发 | - |
