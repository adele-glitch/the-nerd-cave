
<template>
    <div>
        <div class="card bg-dark text-dark text-center mt-2 mb-2">
            <div v-if="product.onSale" class="ribbon ribbon-top-left"><span>sale</span></div>
            <img :src="require(`@/assets/products/${product.imageUrl}`)" class="card-img" alt="...">
            
            <div class="card-body text-center pa-0">
                <button class="btn btn-primary">Add to cart</button>
                <h6 class="card-title mb-0">{{product.itemName}}</h6>
                <p class="card-text mb-2">R {{product.price}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  props: {
    product: Object
  }
}
</script>