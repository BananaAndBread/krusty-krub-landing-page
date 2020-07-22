<template>
  <div class="center">
    <div class="-form">
      <label for="name"> Name</label>
      <input id="name" type="text">
      <label for="email">Email</label>
      <input id="email" type="text">
      <label for="phone">Phone</label>
      <input id="phone" type="text">
      <label for="num-of-persons">Number of persons</label>
      <input id="num-of-persons" type="text">
      <label>Date</label>
      <date-picker v-model="time1" style="width: 100%" value-type="format">
        <template slot="input">
          <input :value="time1" style="width: 100%">
        </template>
        <template slot="icon-calendar">
          <div />
        </template>
        <template slot="icon-clear">
          <div />
        </template>
      </date-picker>
      <ReserveTable class="reserve-table-button-form" />
    </div>
  </div>
</template>

<script>
import DatePicker from 'vue2-datepicker'
import 'vue2-datepicker/index.css'
import 'vue-select/dist/vue-select.css'
import ReserveTable from './Buttons/ReserveTable'
import timeOptions from '@/assets/timeOptions'

export default {
  components: { ReserveTable, DatePicker },
  data () {
    return {
      time1: null,
      timeOptions
    }
  }
}
</script>

<style scoped>
  input{
    border: 2px rgb(204, 204, 204) solid;
    border-radius: 4px;
    height: 2.5em;
    margin-bottom: 1em;
    width: 100%;
    padding-left: 1em;
    color: rgb(128, 128, 128);;
  }
  input:focus{
    border: 2px #DB9A64 solid;
    outline: none;
  }
  .-form{
    display: flex;
    flex-direction: column;
    width: 75%;
  }
  .center{
    display: flex;
    justify-content: center;
    margin-bottom: 40px;
  }
  label{
    color: rgb(128, 128, 128);
    font-family: "Open Sans",serif;
    font-size: 20px;
    font-weight: 400;
    margin-bottom: 8px;
  }
</style>

<style>
  /*Nu eto tozhe vrode ne ochen*/
  .reserve-table-button-form button{
    background: rgb(219, 154, 100);
    width: 100% !important;
    border: rgb(219, 154, 100) 1px solid;
  }

  .reserve-table-button-form{
    width: 100%;
  }
</style>
