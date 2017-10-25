<template>
  <v-footer class="blue darken-2">
    <v-layout row wrap align-center>
      <v-flex xs12>
        <div class="white--text ml-3">
          Xeno-Studios &copy;{{ currentYear() }}
        </div>
      </v-flex>
    </v-layout>
  </v-footer>
</template>

<script>
export default {
  name: 'Footer',
  data () {
    return {
      year: ''
    }
  },
  methods: {
    currentYear () {
      let year = new Date()
      this.year = year.getFullYear()
      return this.year
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
