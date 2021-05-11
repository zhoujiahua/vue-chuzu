<template>
  <div class="about">
    <div id="container"></div>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {};
  },
  created() {
    this.$nextTick(() => this.onLocationClick());
  },
  mounted() {},
  methods: {
    onHotspotClick(e) {},
    onLocationClick(e) {
      var map = new AMap.Map("container", {
        viewMode: "2D", // 默认使用 2D 模式，如果希望使用带有俯仰角的 3D 模式，请设置 viewMode: '3D',
        zoom: 11, //初始化地图层级
        center: [116.397428, 39.90923], //初始化地图中心点
      });
    },
  },
  components: {},
};
</script>


<style lang="scss" scoped>
#container {
  width: 300px;
  height: 180px;
}
</style>