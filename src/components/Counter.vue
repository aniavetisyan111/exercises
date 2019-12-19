<template>
  <v-row align="center">
    <v-col class="text-center" cols="12" sm="4">
        
        <div class="text-center">
            <v-btn v-bind:color="color" v-on:click="count++" rounded><slot></slot> {{count}}</v-btn>
        </div>
      </v-col>
    </v-row>
</template>

<script>
export default {
    name:"Counter",
    props:{
        color:String
    },

  data: () => ({
      count:0
  })
}
</script>
