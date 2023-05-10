创建具有指定纵横比的响应式容器。
- 使用CSS自定义属性<a href='https://developer.mozilla.org/zh-CN/docs/Web/CSS/aspect-ratio#%E5%BD%A2%E5%BC%8F%E5%AE%9A%E4%B9%89'>
  `--aspect-ratio`</a>来定义希望的纵横比。
- 容器元素设置为 `position:relative` 和`height:0`,用`calc`函数和`aspect-ratio`自定义属性计算容器高度。
- 设置容器的孩子元素 `relative:absolute`，同时用<a href='https://developer.mozilla.org/zh-CN/docs/Web/CSS/object-fit#%E8%A
  F%AD%E6%B3%95'>`object-fit:cover`</a>来填充元素保持容器的纵横比。
  ```
  
  ```
