<script setup>

import { ref } from 'vue'

const listaCompras = ref([
  
{
        id: 1,
        nome: 'Camiseta',
        preco: 49.90,
        quantidade: 0,
    },
    {
        id: 2,
        nome: 'Calça',
        preco: 99.90,
        quantidade: 0,
    },
    {
        id: 3,
        nome: 'Meia',
        preco: 9.90,
        quantidade: 0,
    },
    {
        id: 4,
        nome: 'Sapato',
        preco: 199.90,
        quantidade: 0,
    },
    {
        id: 5,
        nome: 'Boné',
        preco: 29.90,
        quantidade: 0,
    },
    {
        id: 6,
        nome: 'Óculos',
        preco: 99.90,
        quantidade: 0,
    },
    {
        id: 7,
        nome: 'Relógio',
        preco: 299.90,
        quantidade: 0,
    },
    {
        id: 8,
        nome: 'Bermuda',
        preco: 79.90,
        quantidade: 0,
    },
    {
        id: 9,
        nome: 'Cueca',
        preco: 19.90,
        quantidade: 0,
    },
    {
        id: 10,
        nome: 'Meia',
        preco: 9.90,
        quantidade: 0,
    }
])

const carrinhos = ref({
  items: [],
  total: 0,
    
})

function incrementar(index) {
    listaCompras.value[index].quantidade++
  }
  function decrementar(index) {
    if(listaCompras.value[index].quantidade > 0){
      listaCompras.value[index].quantidade--
    }
  }
  
  function adicionar(index) {
    if(listaCompras.value[index].quantidade > 0){
      
      carrinhos.value.items.push(
        {...listaCompras.value[index], preco: listaCompras.value[index].quantidade * listaCompras.value[index].preco}
      );
      
      carrinhos.value.total = carrinhos.value.total + listaCompras.value[index].preco * listaCompras.value[index].quantidade
       
    }
    
  }
</script>

<template>
  <div class="produtos">
    <ul>
      <li class="lista" v-for="(item, index) in listaCompras" :key="item.id">
        <p>Item: {{ item.nome }}</p>
        <p>Preco: {{ item.preco }}</p>
        <p>ID: {{ item.id }}</p>
        <p>quantidade: {{ item.quantidade }}</p>
        <button @click="incrementar(index)">+</button>
        <button @click="decrementar(index)">-</button>
        <button @click="adicionar(index)">Adicionar</button>
      </li>
    </ul>
    <hr>
  </div>

  <div class="carrinhoC">
  <ul>

    <li v-for="item in carrinhos.items">
        <p>Item: {{ item.nome }}</p>
        <p>Preço: {{ item.preco.toFixed(2) }}</p>
        <p>ID: {{ item.id }}</p>
        <p>Quantidade: {{ item.quantidade }}</p>

       
    </li>

    <p> Total:{{ carrinhos.total.toFixed(2) }}</p>
  </ul>
  </div>
</template>

<style scoped>

#editor {
  text-align: left;
  margin-left: 500px;
  margin-right: 500px;
  background-color: rgb(134, 33, 218);
  border-radius: 50px;
  border-style: unset;
  color: rgb(236, 216, 216);
  padding: 70px
}
</style>