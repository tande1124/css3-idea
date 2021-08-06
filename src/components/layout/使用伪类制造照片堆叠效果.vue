<template>
  <div class="bruce before-after" data-title="使用伪类实现照片堆叠">
   <div class="stackthree">
     <img src="https://b-gold-cdn.xitu.io/v3/static/img/normal.0447fe9.png">
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>

.stackthree, 
.stackthree::before,
.stackthree::after {
  border: 6px solid #fff;
  height: 200px;
  width: 200px;
  -webkit-box-shadow: 2px 2px 5px rgba(0,0,0,0.3);  // box阴影
  -moz-box-shadow: 2px 2px 5px rgba(0,0,0,0.3);
  box-shadow: 2px 2px 5px rgba(0,0,0,0.3);
}

.stackthree::before {
  top: 5px;
  left: -15px;
  z-index: -1;
  -webkit-transform: rotate(-10deg);
  -moz-transform: rotate(-10deg);
  -o-transform: rotate(-10deg);
  -ms-transform: rotate(-10deg);
  transform: rotate(-10deg);
}
.stackthree::after {
  top: -2px;
  left: -10px;
  -webkit-transform: rotate(-5deg);
  -moz-transform: rotate(-5deg);
  -o-transform: rotate(-5deg);
  -ms-transform: rotate(-5deg);
  transform: rotate(-5deg);
}

.stackthree::before, 
.stackthree::after {
  background: #768590;
  content: "";
  position: absolute;
  z-index: -1;
}
.stackthree {
  float: left;
  position: relative;
  margin: 50px;
}

</style>