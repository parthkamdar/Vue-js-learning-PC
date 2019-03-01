<template>
  <div class="container">
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
    <div class="row alert-info">
      <p>Info: Click on the box to delete it</p>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote';
export default {
  data: function(){
    return{
      maxQuote: 10,
      quotes: [
        'this is a sample quote'
      ]
    }
  },
  components:{
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote
  },
  methods:{
    newQuote(quote){
      this.quotes.push(quote);
    },
    deleteQuote(index){
      this.quotes.splice(index,1);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.alert-info{
  background-color: black;
  color: #f1f1f1;
  border-radius: 10px;
  width: 70%;
  display: block;
  margin: auto;
  height: 50px;
  line-height: 50px;
  text-align: center;
}
</style>
