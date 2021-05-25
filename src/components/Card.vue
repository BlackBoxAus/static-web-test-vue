<template>
  <div>
    <div class="card" v-for="asset in assets" :key="asset.id">
      <div class="image-container">
        <img :src="asset.download_url" alt="image" />
      </div>
      <div class="info">
        <h4>{{ asset.author }}</h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AssetCard",
  data() {
    return {
      assets: {},
    };
  },
  beforeMount() {
    this.getImages();
  },
  methods: {
    async getImages() {
      const res = await fetch("https://picsum.photos/v2/list");
      const data = await res.json();
      this.assets = data.slice(0, 16);
    },
  },
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  margin: 0.4rem;
  float: left;
  background-color: #e9e9e9;
  width: 20rem;
  border-radius: 4px;
  justify-content: center;
  box-shadow: rgba(60, 64, 67, 0.3) 0px 1px 2px 0px,
    rgba(60, 64, 67, 0.15) 0px 1px 3px 1px;

  .info {
    padding: 0.4rem;
  }

  .image-container {
    img {
      border-top-right-radius: 4px;
      border-top-left-radius: 4px;
      justify-self: center;
      width: 100%;
      height: 12rem;
      object-fit: cover;
    }
  }
}
</style>