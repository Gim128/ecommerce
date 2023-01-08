<template>
  <v-app>
    <navbar-view />
    <v-container fluid>
      <v-row>
        <v-col cols="12">
          <v-card class="mx-auto rounded-xl" flat>
            <v-img src="cover2.png" max-height="100%" max-width="100%" contain>

              <v-card-title class="top ml-10">
                <h2 class="title1">Daily Deals...</h2>
              </v-card-title>

              <v-card-title class=" ml-10 mt-n8">
                <h2 class="title2">Fresh meals...</h2>
              </v-card-title>

              <v-card-text class="ml-10">
                <h3 class="green--text">#Free Delivery</h3>
              </v-card-text>

              <v-card-text class="ml-10">
                <v-row>
                  <v-col cols="4">
                    <v-text-field label="Search your daily meals"
                    class="d-none d-sm-none d-md-flex"
                    filled solo prepend-inner-icon="mdi-magnify" flat rounded outlined success
                    >

                    </v-text-field>
                  </v-col>

                  <v-col cols="2" class="marginLeft">
                    <v-btn color="green" rounded dark x-large class="py-7 d-none  d-sm-none d-md-flex">
                      Search
                    </v-btn>
                  </v-col>

                </v-row>
              </v-card-text>

            </v-img>
          </v-card>

          <v-toolbar flat color="transaprent">
            <v-toolbar-title class="text-h6">
              Category
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn-toggle v-model="toggle_exclusive" group color="#49D9A0">
              <v-btn>
                <v-icon>mdi-chevron-left</v-icon>
              </v-btn>
              <v-btn>
                <v-icon>mdi-chevron-right</v-icon>
              </v-btn>
            </v-btn-toggle>
          </v-toolbar>

          <category />

          <v-toolbar flat color="transparent" class="mt-5">
            <v-toolbar-title class="text-h6">Popular Products</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn rounded color="green" dark class="px-8">See all</v-btn>
          </v-toolbar>

          <products />

        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
import NavbarView from '@/components/NavbarView.vue'
import Category from '@/components/Category.vue'
import Products from '@/components/Products.vue'

export default {
    name: "HomeViewComponent",

    data:() => ({
      toggle_exclusive: 1,
    }),

    components: {
        NavbarView,
        Categor,
        Productsy
    },     
}
</script>

<style>
  .marginLeft{
    margin-left: -90px;
  }
  .mtop {
    margin-top: 100px;
  }
  .mbottom {
    margin-bottom: 100px;
  }
  .v-card.borderme {
    border: 2px solid green !important;
  }
  .v-card.borderout {
    border: 1px solid #d5f0db !important;
  }
  .v-btn:not(.v-btn--round).v-size--default.add {
    min-width: 0px !important;
  }
  .theme--light.v-sheet--outlined.mobile {
    border: 2px solid black !important;
  }
  @media only screen and (max-width: 600px){
    h2.title1{
      font-size: 15px;
    }
    h2.title2 {
      font-size: 15px;
    }
  }
  @media only screen and (min-width: 600px) {
    .top {
      margin-top: 70px;
    }
  }
  @media only screen and (min-width: 768px) {
    .top {
      margin-top: 120px;
    }
  }
</style>