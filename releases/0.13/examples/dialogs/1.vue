<template>
  <v-layout row justify-center style="position: relative;">
    <v-dialog v-model="dialog" lazy absolute>
      <v-btn primary dark slot="activator">Open Dialog</v-btn>
      <v-card>
        <v-card-title>
          <div class="headline">Use Google's location service?</div>
        </v-card-title>
        <v-card-text>Let Google help apps determine location. This means sending anonymous location data to Google, even when no apps are running.</v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn class="green--text darken-1" flat="flat" @click.native="dialog = false">Disagree</v-btn>
          <v-btn class="green--text darken-1" flat="flat" @click.native="dialog = false">Agree</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-layout>
</template>

<script>
  export default {
    data () {
      return {
        dialog: false,
        test: true
      }
    }
  }
</script>
