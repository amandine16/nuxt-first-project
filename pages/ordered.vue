<template>
  <div>
    <h1 class="display-1 title">Commander</h1>
    <h2 class="h2">Produits disponibles</h2>
    <div class="card-deck">
      <Product
        v-for="produit in products"
        :key="produit.id"
        :name="produit.name"
        :price="produit.price"
        v-on:ordered="addProduct"
        role="order"
      />
    </div>
    <!-- Shopping cart -->
    <h2 class="h2">Produits commandés</h2>
    <div class="card-deck">
      <Product
        v-for="produit in ordered"
        :key="produit.id"
        :name="produit.name"
        :price="produit.price"
        role="display"
      />
    </div>
  </div>
</template>

<script>
// Import Components
import Product from "@/components/Product.vue";
// DATA
export default {
  components: {
    Product
  },
  data() {
    return {
      products: [
        { name: "Pizza", price: "12.00", id: 0 },
        { name: "Hamburger", price: "9.50", id: 1 },
        { name: "Frites", price: "2.50", id: 2 },
        { name: "Salade", price: "8.00", id: 3 }
      ],
      ordered: [{ name: "Frites", price: "2.50" }]
    };
  },
  methods: {
    addProduct(name, price) {
      this.ordered.push({ name, price });
    }
  }
};
</script>

<style>
.card-deck {
  align-items: center;
  margin: 45px 0;
}
.title {
  color: var(--greenDark) !important;
}
.h2 {
  color: var(--greenHover);
}
</style>
