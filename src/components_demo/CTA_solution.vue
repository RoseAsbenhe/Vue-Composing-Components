<template>
  <button
    :class="{'btn-cta--disabled': !isActive}"
    @click.prevent="clickHandler()"
    class="btn btn--full btn-cta btn-cta--green"
  >
    Add to Cart
  </button>
</template>

<script>
import { add } from 'lodash';

export default {
  name: 'CTA',
  data() {
    return {
      isActive: true,
			counter: 0,
    };
  },
  methods: {
		clickHandler() {
			if (this.isActive) {
				this.addToCart();
			}
			this.counter = add(this.counter, 1);
			this.isActive = !this.isActive;
		},
    addToCart() {
			// add item to cart
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
