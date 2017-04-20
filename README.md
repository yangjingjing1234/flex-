# flex-
css3 ,flex简单应用
## flex圣杯布局
> 1,主要原理就是固定一个侧栏，领一个侧栏可随意分配剩余空间flex:1;就简单满足随意分配剩余空间
>
> 2,固定的那个侧栏直接给个宽度就能满足，例子如下所示
>
> 3,在高深一点flex:0 0 50px;就是不分配剩余空间，不缩小项目,他的设置跟宽度设置选其一就行
>

``` 
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style type="text/css">
		.box{
			width: 200px;
			display: flex;
			height: 200px;
			background: red;
		}

	/*	flex属性是
	flex-grow, 
	flex-shrink 
	和 flex-basis的简写，
	默认值为0 1 auto。
	后两个属性可选。*/

		.item{
			/*flex:0 1 auto;*/
			/*flex-grow: 1; */
			/*0即如果存在剩余空间，也不放大,分配剩余空间比率因子*/
			/*flex-shrink:1;*/
			/*1即如果空间不足，该项目将缩小。根据弹性盒子元素所设置的收缩因子作为比率来收缩空间。*/
			/*flex-basis:100px;*/
			/*flex-grow:1的情况下，分配多余空间之前，项目占据的主轴空间（main size）,小于均分值就均分，大于均分值，就按设置的最大值来算*/
      /* flex-grow:0的情况下，如果只是设置给某一个元素，那么这个元素就是固定100px宽度 */
			
		}
		.side1{
			width: 50px;
			height: 100px;
			background: blue;
			overflow: hidden;
			/*flex:0 0 50px;*/
			/*flex-grow: 2;*/
		}
		.side2{
			flex:1;
			height: 100px;
			background: yellow;
		}

	</style>
</head>
<body>
	<div class="box">
		<div class="item side1">11111111111111111111</div>
		<div class="item side2">22</div>
	</div>
</body>
</html>
``` 
