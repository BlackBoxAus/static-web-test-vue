<template>
  <div class="gallery-container">
    <div class="gallery-text">
      <h3>Gallery</h3>
      <p>We certainly have a lot of images.</p>
    </div>
    <div class="gallery-images">
      <div>
        <asset-card />
      </div>
    </div>
  </div>
</template>

<script>
import AssetCard from "../components/Card.vue";
export default {
  name: "Gallery",
  components: {
    AssetCard,
  },
};
</script>

<style lang="scss" scoped>
.gallery-container {
  padding: 0.5rem;
  background-color: #f3f3f3;
  display: flex;
  flex-direction: column;
  height: 95vh;
  overflow-y: scroll;
  .gallery-images {
    margin-top: 0.5rem;
  }
}
</style>