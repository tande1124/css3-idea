<template>
  <div class="bruce flex-ct-x" data-title="使用float排版环绕文本">
    <div class="text-wrap">
      <img src="">
      hello,这里使用float的用法，XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.text-wrap {
  overflow: hidden;
	width: 400px;
	height: 300px;
	font-size: 20px;
	color: #f66;
	word-break: break-all;
	img {
		float: left;
		height: 200px;
    width: 200px;
    background-color:blue;
	}
}

</style>