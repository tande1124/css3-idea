<template>
  <div class="home">
    <div class="content layout">
			<layout1></layout1>
		</div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Layout1 from "@/components/layout/使用clip-path排版蜂窝布局.vue";

export default defineComponent({
  name: 'Home',
  components: {
    Layout1,
  },
});
</script>
