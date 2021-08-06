<template>
  <div class="bruce" data-title="使用letter-spacing排版倒序文本">
    <div class="reverse-text">前端小练习</div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.reverse-text {
  padding: auto;
  font-weight: bold;
  font-size:50px;
  color: pink;
  letter-spacing: 100px;  //letter-spacing最少是font-size的2倍  字体之间的间隔
}

</style>