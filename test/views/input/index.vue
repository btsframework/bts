<template>
  <section>
    <h2 style="margin-bottom: 100px">Input</h2>
    <v-input v-model="input1"></v-input>
    <br>
    <br>
    <br>
    <v-input size="large" placeholder="large size"/>
    <v-input placeholder="default size"/>
    <v-input size="small" placeholder="small size"/>
    <br>
    <br>
    <br>
    <v-input icon="search" placeholder="Input" style="width: 200px"></v-input>
    <br>
    <br>
    <br>
    <v-input type="textarea" :rows="4" placeholder="Input"></v-input>
    <br>
    <br>
    <br>
    <v-input type="textarea" :autosize="true" placeholder="Input"></v-input>
    <br>
    <br>
    <br>
    <v-input type="textarea" :autosize="{minRows: 2,maxRows: 5}" placeholder="Input"></v-input>
<br>
    <br>
    <br>
    <v-input placeholder="Input" style="width: 300px">
      <template slot="prepend">Http://</template>
      <template slot="append">.com</template>
    </v-input>
  </section>
</template>
<script>
/* eslint-disable */
  export default {
    data() {
      return {
        input1: 'xxx'
      }
    },
    watch: {
      input1() {
        console.log(this.input1)
      }
    }
  }
</script>
