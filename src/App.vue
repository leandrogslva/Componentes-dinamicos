<template>
<div class ="app">
  <div class="row">
    <div class="col-xs-12">
      <button @click="selectedComponent = 'appQuote'">Quote</button>
      <button @click="selectedComponent = 'appAuthor'">Author</button>
      <button @click="selectedComponent = 'appNew'">New</button>
      <hr>
      <p>{{selectedComponent}}</p>

      <!-- o comando "component" neste caso permite que usemos os nosso componentes de maneira dinamica -->
      <!-- o comando "keep-alive" permite que o componente não seja destruido caso você acesse outra parte do seu site -->
      <keep-alive>
      <component :is="selectedComponent">
      <p>Default</p>
      </component>
      </keep-alive>

     <!--  <appQuote>
        <h2 slot="title">{{quoteTitle}}</h2>
        <p>A wonderful quote</p>  
      </appQuote> -->

<!-- Este comando é utilizado através do props
    <appQuote quote="A wonderful quote!"></appQuote> -->
    
    </div>
  </div>
</div>
</template>

<script>
import Quote from './components/Quote.vue';
import Author from './components/Author.vue';
import New from './components/New.vue';

export default {
  data: function() {
  return {
    quoteTitle: 'The Quote',
    selectedComponent: 'appQuote'
  }
},
  components: {
    appQuote: Quote,
    appAuthor: Author,
    appNew: New
  },
};
</script>

<style>

</style>
