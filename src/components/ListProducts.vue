<template>
  <div>
    <div class="container">
      <h1>List Products</h1>
      <table class="table table-striped">
        <thead>
          <tr>
            <th>ID</th>
            <th>NAME</th>
            <th>PRICE</th>
            <th>DESCRIPTION</th>
            <th>Edit</th>
            <th>Delete</th>
          </tr>
        </thead>
        <tbody>
          <tr
            v-for="product in this.products"
            :key="product.id"
            v-on:click.prevent="onEdit(product)"
          >
            <td>{{ product.id }}</td>
            <td>{{ product.Name }}</td>
            <td>{{ product.Price }}</td>
            <td>{{ product.Description }}</td>
            <td><button type="button" class="btn btn-danger">Edit</button></td>
            <td>
              <button
                type="button"
                class="btn btn-danger"
                v-on:click.stop="onRemove(product.id)"
              >
                Delete
              </button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "ListProducts",
  data() {
    return {};
  },
  components: {},
  props: ["products"],
  methods: {
    onRemove(productId) {
      //console.log(productId);
      this.$emit("remove", productId);
    },
    onEdit(product) {
      //console.log(product);
      this.$emit("edit", product);
    },
  },
};
</script>

<style lang="scss" scoped>
</style>