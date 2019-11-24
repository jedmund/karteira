<template>
  <div class="page">
    <div id="header">
      <h1>Karteira</h1>
    </div>
    
    <div class="weapon-grid">
      <grid-mainhand @click.native="open" />

      <div class="weapons">
        <grid-unit @click.native="open"/>
        <grid-unit @click.native="open" />
        <grid-unit @click.native="open" />
        <grid-unit @click.native="open" />
        <grid-unit @click.native="open" />
        <grid-unit @click.native="open" />
        <grid-unit @click.native="open" />
        <grid-unit @click.native="open" />
        <grid-unit @click.native="open" />
      </div>
    </div>

    <modal name="example">
      <div class="basic-modal">
        <h1 class="title">Modal Title</h1>
        <button class="button" type="button" @click="close">Close Modal</button>
      </div>
    </modal>
  </div>
</template>

<script lang="ts">
  import GridMainhand from '~/components/grid-mainhand.vue'
  import GridUnit from '~/components/grid-unit.vue'
  import VueThinModal from 'vue-thin-modal'

  export default {
    components: {
      GridMainhand,
      GridUnit
    },

    methods: {
      open () {
        console.log("Clicked");
        this.$modal.push('example')
      },

      close () {
        console.log("Closed");
        this.$modal.pop()
      }
    }
  }
</script>

<style>
  .page {
    margin: 0 auto;
    width: 561px;
  }

  #header {
    margin-top: 24px;
    height: 44px;
  }

  .icon.plus {
    display: block;
    fill: #C0AA88;
    margin: 0 auto;
    height: 20px;
    width: 20px;
  }

  .weapon-grid {
    display: flex;
    margin-top: 48px;
  }

  .weapons {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    width: 378px;
  }

  .weapons > * {
    margin-bottom: 72px;
    margin-right: 24px;
   
  }

  .weapons > *:nth-child(3n+3) {
    margin-right: 0;
  }
</style>
