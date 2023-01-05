<template>
  <v-app>
    <navbar-view />
    <v-container fluid>
      
    </v-container>
  </v-app>
</template>

<script>
import NavbarView from '@/components/NavbarView.vue'

export default {
    name: "HomeViewComponent",

    components: {
        NavbarView
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