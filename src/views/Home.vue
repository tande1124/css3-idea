<template>
  <div class="home">
    <div class="content layout">
			<layout1></layout1>
      <layout2></layout2>
      <layout3></layout3>
      <layout4></layout4>
		</div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Layout1 from "@/components/layout/使用clip-path排版蜂窝布局.vue";
import Layout2 from "@/components/layout/使用flexbox排版各种布局.vue";
import Layout3 from "@/components/layout/使用float排版环境文本.vue";
import Layout4 from "@/components/layout/使用伪类制造照片堆叠效果.vue";

export default defineComponent({
  name: 'Home',
  components: {
    Layout1,
    Layout2,
    Layout3,
    Layout4,
  },
});
</script>

<style lang="scss">
::-webkit-scrollbar {
	width: 6px;
	height: 6px;
}
::-webkit-scrollbar-track {
	background-color: rgba(#ccc, .3);
}
::-webkit-scrollbar-thumb {
	border-radius: 3px;
	background-color: #ccc;
}
.bruce {
	overflow: hidden;
	position: relative;
	padding: 50px 0;
	border-bottom: 1px solid #ccc;
	min-height: 300px;
	&::before {
		position: absolute;
		left: 50%;
		top: 0;
		padding: 0 10px;
		border-radius: 0 0 5px 5px;
		max-width: 300px;
		line-height: 20px;
		color: #fff;
		content: attr(data-title);
		transform: translateX(-50%);
	}
	&::after {
		position: absolute;
		right: 0;
		bottom: 0;
		padding: 5px 10px;
		border-top-left-radius: 5px;
		background-color: #ccc;
		font-weight: bold;
		font-size: 16px;
		color: #fff;
	}
}
.content {
	overflow: auto;
  margin: auto;
	transition: all 300ms;
	&.layout .bruce {
		&::before {
			background-color: #f66;
		}
		&::after {
			content: "布局";
		}
	}
}
</style>
