<template>
  <v-container fluid>
    <v-row>
      <v-col cols="12">
        <v-row
          align="center"
          justify="center"

          class="grey lighten-5 text-center"
          style="height: 100vh;"
        >
          
            <h1>Marketing digital</h1>
          
         
        </v-row>
      </v-col>
      <v-col cols="12">
        <v-row justify="center">
          <v-col
            cols="6"
            md="2"
          >
            <v-select
              v-model="alignment"
              :items="alignmentsAvailable"
              label="Align"
            ></v-select>
          </v-col>

          <v-col
            cols="6"
            md="2"
          >
            <v-select
              v-model="justify"
              :items="justifyAvailable"
              label="Justify"
            ></v-select>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {

}
</script>

<style>

</style>