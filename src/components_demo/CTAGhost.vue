<template>
  <button
    :class="{'btn-cta--disabled': !isActive}"
    :disabled="!isActive"
    @click.prevent="addToCart()"
    class="btn btn--full btn-cta btn-cta--ghost"
  >
    Add to Cart
  </button>
</template>

<script>
export default {
  name: 'CTAGhost',
  data() {
    return {
      isActive: true,
    };
  },
  methods: {
    addToCart() {
      if (this.isActive) {
        // add item to cart
      }
      this.isActive = !this.isActive;
    },
  },
};
</script>

<style scoped>
.btn {
  cursor: pointer;
  display: inline-block;
  text-align: center;
  text-decoration: none;
}

.btn-cta {
  font-size: 16px;
  padding: 15px 32px;
}

.btn-cta--ghost {
  background-color: white;
  border: 1px solid #64B587;
  color: #64B587;
}

.btn-cta--disabled {
  background-color: #ddd;
}
</style>
