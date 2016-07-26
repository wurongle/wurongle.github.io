# layout
### flex

- 与CSS的flexbox的默认值差异:
  - **flexDirection** defaulting to **column** instead of **row**
  - **alignItems** defaulting to **stretch** instead of **flex-start**
  - **flex** parameter only supports **asingle number**
- flexDirection,取值有**row** / **row-reverse** / **column** / **column-reverse** 
- justifyContent, 作用于flexDirection主轴子容器，取值有**flex-start** / **center** / **flex-end** / **space-around**(两端对齐)/ **space-between**
- alignItems, 作用于非flexDirection侧轴子容器，取值有**flex-start** / **center** / **flex-end** / **stretch**(拉伸)
- alignSelf, 作用于非flexDirection侧轴容器，默认值是**auto**,取值同alignItems + **auto**
- flexWrap, 作用于子容器，定义子元素是否折行，取值有**wrap** / **nowrap**
