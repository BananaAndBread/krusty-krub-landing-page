<template>
  <div>
    <div class="center">
      <div class="tabs">
        <div v-for="tab in tabs" :key="tab" class="tab" :class="{tab: true, 'tab-active': tab===activeTab}" @click="setActive(tab)">
          <slot :name="'tab-head-'+tab" />
        </div>
      </div>
    </div>
    <div class="tab-contents">
      <div v-for="tab in tabs" :key="tab" :style="{display: tab===activeTab?'block':'none'}" :class="{'tab-content': true}">
        <slot :name="'tab-content-'+tab" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Tab',
  components: {
  },
  props: {
    initialTab: String,
    tabs: Array
  },
  data () {
    return {
      activeTab: ''
    }
  },
  mounted () {
    if (!this.initialTab) {
      this.activeTab = this.tabs[0]
    } else {
      this.activeTab = this.initialTab
    }
  },
  methods: {
    setActive (tab) {
      this.activeTab = tab
    }
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
  .center{
    display: flex;
    justify-content: center;
    border-bottom: solid gray 1px;
  }
  .tabs{
    display: flex;
  }
  .tab{
    margin-left: 1em;
    margin-right: 1em;
    display: flex;
    flex-direction: column;
    align-items: center;
    box-sizing:border-box;
    cursor:pointer;
    color:rgb(89, 102, 114);
    font-family:Poppins, sans-serif;
    font-size:16px;
    font-style:normal;
  }
  .tab p {
    margin-bottom: 1em;
  }
  .tab-active {
    border-bottom: rgb(219, 154, 100) 1px solid;
    color: rgb(219, 154, 100);;
  }
</style>
