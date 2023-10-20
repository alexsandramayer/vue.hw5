<template>
    <div class="product">
        <h2>{{ product.name }}</h2>
        <div>{{ formattedPrice}}</div>
        <p v-if="product.available">Available</p>
        <p v-else>Out of stock</p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                product: 
                    {
                        name: 'apple',
                        price: 99.99,
                        available: false,
                    } 
            }
        },
        computed: {
            formattedPrice: function() {
                return `$ ${this.product.price}`;
            }
        },
    }
</script>

<style lang="scss" scoped>
    .product{
        display: block;
        margin-left: 100px;
    }
</style>