<template>
  <div id="map"></div>
</template>
<script setup>
import MindElixir from "mind-elixir";
import "mind-elixir/style";
import example from "mind-elixir/example";
import { onMounted, ref } from "vue";

const me = ref();
onMounted(() => {
  me.value = new MindElixir({
    el: "#map",
  });
  me.value.init(example);
});
</script>
<style lang="less" scoped>
#map {
  width: 100%;
  height: 500px;
}
</style>
