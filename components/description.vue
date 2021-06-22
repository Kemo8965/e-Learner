<template>
  <div class="text-center">
    <v-dialog
      v-model="dialog"
      width="500"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="info"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Description
        </v-btn>
      </template>

      <v-card>
        <v-card-title class="text-h5 grey lighten-2">
         Intro To Mathematics
        </v-card-title>

        <v-card-text>
           {{ desc }}
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="primary"
            text
            @click="dialog = false"
          >
            Okay, got it!
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>
<script>
  export default {
    data () {
      return {
        dialog: false,

        desc:"Even though everyone learns mathematics at school, it is difficult to define exactly what mathematics is. Clearly numbers, shapes and equations form part of it, but only a small part compared to the vast space of mathematical concepts and ideas. The best way to understand what mathematics is and what mathematicians work on – is to do mathematics."
      }
    },
  }
</script>