<template>
  <section>
    <ComponentAdd :product="productInForm" v-on:submit="onFormSave" />
    <ListProducts
      :products="products"
      v-on:remove="onRemoveClicked"
      v-on:edit="onEditClicked"
    />
  </section>
</template>

<script>
import ListProducts from "./ListProducts";
import ComponentAdd from "./ComponentAdd";
import uuid from "uuid";
const initialData = () => {
  return {
    productInForm: {
      id: null,
      Name: "",
      Description: "",
      Price: null,
    },
    products: [
      {
        id: uuid.v4(),
        Name: "Dess",
        Price: "32",
        Description: "truong.le2241199@gmail.com",
      },
      {
        id: uuid.v4(),
        Name: "Dess",
        Price: "32",
        Description: "truong.le2241199@gmail.com",
      },
      {
        id: uuid.v4(),
        Name: "Dess",
        Price: "32",
        Description: "truong.le2241199@gmail.com",
      },
    ],
  };
};
export default {
  components: {
    ListProducts,
    ComponentAdd,
  },
  data: initialData,
  methods: {
    onFormSave(product) {
      // Generate an id using the third-party lib 'uuid'
      //   product.id = uuid.v4();
      //   // add it to the product list
      //   console.log(product);
      //   this.products.push(product);
      //   // reset the form
      //   this.resetProductInForm();
      const index = this.products.findIndex((p) => p.id === product.id);
      if (index !== -1) {
        this.products.splice(index, 1, product);
      } else {
        product.id = uuid.v4();
        this.products.push(product);
      }
      this.resetProductInForm();
    },

    resetProductInForm() {
      this.productInForm = initialData().productInForm;
    },

    //remove
    onRemoveClicked(productId) {
      const index = this.products.findIndex((p) => p.id === productId);

      this.products.splice(index, 1);

      if (productId === this.productInForm.id) {
        this.resetProductInForm();
      }
    },
    //edit
    onEditClicked(product) {
      //console.log([...product]);
      this.productInForm = { ...product };
    },
  },
};
</script>

<style lang="scss" scoped>
</style>