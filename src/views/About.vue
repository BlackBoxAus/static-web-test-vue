<template>
  <div class="about-container">
    <h3>About Us</h3>
    <p>
      We are Australia's largest timelapse provider based in Brisbane. <br />
      This is us testing our new dashboard.
    </p>
    <br />
    <p>Have a look at our <router-link to="/gallery">Gallery.</router-link></p>
  </div>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped lang="scss">
.about-container {
  display: flex;
  background-color: #f3f3f3;
  display: flex;
  flex-direction: column;
  padding: 0.5rem;

  h3 {
    margin-bottom: 0.4rem;
  }
  p {
    font-size: 1rem;
    line-height: 1.25rem;
  }
}
</style>