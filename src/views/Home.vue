<template>
  <div class="container">
    <h3>Home</h3>
    <p>This is an example that showcases components and vue router.</p>
    <br />
    <!-- Importing a placeholder data table from components -->
    <DataTable />
  </div>
</template>

<script>
import DataTable from "../components/Table.vue";
export default {
  name: "Home",
  components: { DataTable },
};
</script>

<style lang="scss" scoped>
.container {
  background-color: #f3f3f3;
  padding: 0.5rem;
  h3 {
    margin-bottom: 0.5rem;
  }

  h4 {
    margin-top: 0.5rem;
  }
}
</style>