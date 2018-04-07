<template>
  <div>
    <ul class="wrapper">
      <li v-for="(data,index) in datas" :key="index" class="list">
        {{data.text}}
      </li>
    </ul>
    <button @click="currentPage=0" :style="buttonStyles">
      «
    </button>
    <button v-for="n in calc" :key="n*3" @click="currentPage=n-1" v-if="n-1 < currentPage + 4 && n-1 > currentPage - 4"  :style="[buttonStyles, {background: n-1== currentPage ? activeButtonColor :'transparent'}]" >
      {{n}}
    </button>
    <button @click="currentPage=calc-1" :style="buttonStyles">
      »
    </button>
  </div>
</template>

<script>
  export default {
    name: 'Paginations',
    props: {
      perItem: {
        type: String,
        required: true
      },
      data: {
        type: Array,
        default: function () { return [] }
      },
      buttonStyles: {
        type: Object,
        default: function () { return {} }     
      },
      activeButtonColor: {
        type: String,
        default: 'transparent' 
      }
    },
    data() {
      return {
        datas: this.data,
        currentPage: 0
      }
    },
    computed: {
      calc() {
        return Math.ceil(this.data.length / this.perItem)
      }
    },
    watch: {
      currentPage() {
        const val = this.currentPage * +this.perItem
        this.datas = this.data.slice(val, val + +this.perItem );
      }
    },
    created() {
      const val = this.currentPage * +this.perItem
      this.datas = this.data.slice(val, val + +this.perItem)
    },
    mounted() {
      console.log(this.calc)
    }
  }
</script>

<style>
  .wrapper {
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 5px;
  }
  .list {
    box-sizing: border-box;
    justify-self: center;
    display: block;
    width: min-content;
    border: 1px solid #ddd;
    padding: 8px 10px;
    font-size: 13px;
    line-height: 16px;
  }
</style>
