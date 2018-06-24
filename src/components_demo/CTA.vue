<template>
  <button
    :class="{'btn-cta--disabled': !isActive}"
    :disabled="!isActive"
    @click.prevent="addToCart()"
    class="btn btn-cta btn--full-width btn-cta--green"
  >
    Add to Cart
  </button>
</template>

<script>
export default {
  name: 'CTA',
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

.btn-cta--green {
  background-color: #64B587;
  border: none;
  color: white;
}

.btn-cta--disabled {
  background-color: #ddd;
}
</style>
