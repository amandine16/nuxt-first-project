<template>
  <div class="card text-white bg-dark mb-3" style="max-width: 18rem">
    <div class="card-header">{{ name }}</div>
    <div class="card-body">
      <p class="card-text">{{ price }} €</p>
      <!-- send information from component to the container "Ordered", with display condition for a button -->
      <button
        v-if="role == 'order'"
        @click="$emit('ordered', name, price)"
        class="btn"
      >
        Commander
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Product",
  props: ["name", "price", "role"]
};
</script>

<style>
.card {
  min-width: 150px;
  max-width: 100% !important;
}
.btn {
  background: var(--green);
  color: white;
}
</style>
