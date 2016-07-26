# layout
### flex

- 与CSS的flexbox的默认值差异:
  - **flexDirection** defaulting to **column** instead of **row**
  - **alignItems** defaulting to **stretch** instead of **flex-start**
  - **flex** parameter only supports **asingle number**

- justify content, 作用于flexDirection主轴子容器，取值有**flex-start** / **center** / **flex-end** / **space-around**(两端对齐)/ **space-between**
- align items, 作用于非flexDirection侧轴子容器，取值有**flex-start** / **center** / **flex-end** / **stretch**(拉伸)
- align self, 作用于非flexDirection侧轴容器，取值同align items
