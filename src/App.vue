<template>
  <div id="app">
    <paginationComp perItem="5" :data="datas" :buttonStyles="btnStyles" activeButtonColor="#2a5ebe"></paginationComp>
  </div>
</template>

<script>
import Paginate from './Components/Pagination.vue'
  export default {
    name: 'app',
    data() {
      return {
        datas: [
          {id:1, text:'selamar1'},
          {id:2, text:'selamar2'},
          {id:3, text:'selamar3'},
          {id:4, text:'selamar4'},
          {id:5, text:'selamar5'},
          {id:6, text:'selamar6'},
          {id:7, text:'selamar7'},
          {id:8, text:'selamar8'},
          {id:9, text:'selamar9'},
          {id:10, text:'selamar10'},
          {id:11, text:'selamar11'},
          {id:12, text:'selamar12'},
          {id:13, text:'selamar13'},
          {id:14, text:'selamar14'},
          {id:15, text:'selamar15'},
          {id:16, text:'selamar16'},
          {id:17, text:'selamar17'},
          {id:18, text:'selamar18'},
          {id:19, text:'selamar19'},
          {id:20, text:'selamar20'},
          {id:21, text:'selamar21'},
          {id:22, text:'selamar22'},
          {id:23, text:'selamar23'},
          {id:24, text:'selamar24'},
          {id:25, text:'selamar25'},
          {id:26, text:'selamar26'},
          {id:27, text:'selamar27'},
          {id:28, text:'selamar28'},
          {id:29, text:'selamar29'},
          {id:30, text:'selamar30'},
          {id:31, text:'selamar31'},
          {id:32, text:'selamar32'},
          {id:33, text:'selamar33'},
          {id:34, text:'selamar34'},
          {id:35, text:'selamar35'},
          {id:36, text:'selamar36'},
          {id:37, text:'selamar37'},
          {id:38, text:'selamar38'},
          {id:39, text:'selamar39'},
          {id:40, text:'selamar40'},
          {id:41, text:'selamar41'},
          {id:42, text:'selamar42'},
        ],
        btnStyles: {
          boxSizing: 'border-box',
          cursor:'pointer',       
          border: '1px solid #ddd',
          verticalAlign:'center',
          background: 'transparent',
          padding: '8px 10px',
          fontSize: '14px',
          lineHeight: '10px',
          height: '30px',
          //marginRight:'5px'
        }
      }
    },
    components: {
      paginationComp: Paginate,
    }
  }
</script>

<style>
  #app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

  h1,
  h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>
