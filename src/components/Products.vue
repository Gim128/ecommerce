<template>
    <v-row justify="center" class="space px-16">
        <v-col cols="12" xs="12" sm="6" md="4" v-for="(product, i) in products" :key="i">
            <v-card class="mx-auto rounded-xl" max-width="300" flat outlined>
                <div align="center" justify="center">
                    <v-img max-height="300" max-width="300" contain :src="product.img"></v-img>
                </div>
                <v-card-title>{{product.title}}</v-card-title>
                <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">{{ product.subtitle }}</v-card-title>.
                <v-card-title class="mt-n4">{{product.price}}</v-card-title>
                <v-card-actions class="mw-2 mt-n4">
                    <v-btn outlined class="mt-n2 add">
                        <v-icon color="green" @click="decrement">mdi-minus</v-icon>
                    </v-btn>
                    <strong class="mx-2" v-text="bpm"></strong>
                    <v-btn outlined class="mt-n2 add">
                        <v-icon color="green" @click="increment">mdi-plus</v-icon>
                    </v-btn>
                    <v-spacer></v-spacer>
                    <v-btn class="mx-2 mt-n3" fab dark small color="green">
                        <v-icon dark>mdi-shopping</v-icon>
                    </v-btn>

                    <!-- 29:34 -->
                </v-card-actions>
            </v-card>
        </v-col>
    </v-row>
</template>
    
<script>
export default {
    name: "ProductsView",

    data: () => ({
        bpm: 1,
        products: [
            {img: "pr1.png", title: "cabbage", subtitle: "1Kg", price:"Rs.110.00"},
            {img: "pr2.png", title: "Perry's Ice Cream", subtitle: "1Kg", price:"Rs.400.00"},
            {img: "pr3.png", title: "Potato", subtitle: "1Kg", price:"Rs.160.00"},
            {img: "pr4.png", title: "Bundle Pack", subtitle: "Potato", price:"Rs.180.00"},
            {img: "pr5.png", title: "orio Biscuit", subtitle: "270g", price:"Rs.120.00"},
            {img: "pr6.png", title: "Papaya", subtitle: "1Kg", price:"Rs.130.00"},
        ]
    }),

    methods: {
        decrement() {
            this.bpm--
        },
        increment() {
            this.bpm++
        }
    }

}
</script>

<style>

</style>