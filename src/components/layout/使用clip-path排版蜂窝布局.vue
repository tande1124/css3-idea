<template>
   <div class="bruce flex-ct-x" data-title="使用clip-path排版蜂窝布局">
    <div class="cellular-layout" style="--count: 16">
			<label for="a" style="--index: 0">0</label>
			<label class="a" style="--index: 1">1</label>
			<label class="a" style="--index: 2">2</label>
			<label class="a" style="--index: 3">3</label>
			<label for="b" style="--index: 4">4</label>
			<label class="b" style="--index: 5">5</label>
			<label class="b" style="--index: 6">6</label>
			<label class="b" style="--index: 7">7</label>
			<label for="c" style="--index: 8">8</label>
			<label class="c" style="--index: 9">9</label>
			<label class="c" style="--index: 10">10</label>
			<label class="c" style="--index: 11">11</label>
			<label for="d" style="--index: 12">12</label>
			<label class="d" style="--index: 13">13</label>
			<label class="d" style="--index: 14">14</label>
			<label class="d" style="--index: 15">15</label>
		</div>
   </div>
</template>

<script>
export default  {

}
</script>

<style lang="scss" scoped>
.cellular-layout {
	display: flex;
	flex-wrap: wrap;
	justify-content: center;
	margin-top: -50px;
	width: 400px;
	text-align: center;
	label {
		--Θ: calc(var(--index) / var(--count) * 1turn);
		margin-left: -15px;
		width: 100px;
		height: 100px;
		background-color: #3c9;
		filter: hue-rotate(var(--Θ));  // filter: 滤镜 hue-rotate()函数是一个内置函数，用于对图像应用滤镜以设置图像的色调旋转
		clip-path: polygon(25% 5%, 75% 5%, 100% 50%, 75% 95%, 25% 95%, 0 50%);  // clip-path 直译过来就是裁剪路径，使用SVG或形状定义一个HTML元素的可见区域的方法
		cursor: pointer;
		line-height: 100px;
		font-size: 20px;
		color: #fff;
		&:nth-child(even) {
			transform: translateY(50px);
		}
		&:nth-child(4n-3) {
			margin-left: 0;
		}
	}
}
</style>