1.使用position属性将元素的左上角定位到页面的中心点,transform移动元素中心点到页面中心点,注意为父元素设置定位
```
.center {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
```
2.使用flexbox布局，将元素放在一个固定的容器中，并设置该容器的display属性为flex，justify-content和align-items属性都设置为center
```
<!DOCTYPE html>
<html>
<head>
<title>页面标题</title>
<style>
  .center {
    display: flex;
    justify-content: center;
    align-items: center;
    height:300px;
    background-color:#999;
  }
</style>
</head>
<body>
<div class="center">
<h1 >这是一个标题</h1>
</div>
</body>
</html>
```
3.使用grid布局，将元素放在一个固定的容器中，并设置该容器的display属性为grid，将元素放在容器的中央单元格
```
<!DOCTYPE html>
<html>
<head>
<title>页面标题</title>
<style>
  .container {
    display: grid;
    background-color:#eee;
    height:300px;
  }
  .center {
      grid-row: 1 / 2;
      grid-column: 1 / 2;
      justify-self: center;
      align-self: center;
  }
</style>
</head>
<body>

<div class="container">
<h1 class="center">这是一个标题</h1>
</div>

</body>
</html>
```
