<script setup>

import { ref } from 'vue'
const listaCompras = ref([

{
        id: 1,
        nome: 'Livro- Manifesto do partido comunista',
        preco: 49.90,
        quantidade: 0,
        img:"https://queissocamarada.com/loja/wp-content/uploads/2020/03/camisa-CCCP-vermelha.jpg"
    },
    {
        id: 2,
        nome: 'Adesivo-Marx',
        preco: 99.90,
        quantidade: 0,
        img:"https://queissocamarada.com/loja/wp-content/uploads/2018/11/Poster_1.deMaio.png"
    },
    {
        id: 3,
        nome: 'Body-Fantasma Comunista',
        preco: 9.90,
        quantidade: 0,
        img:"https://queissocamarada.com/loja/wp-content/uploads/2021/10/Body-verao-Marx-Vermelo.jpg"
    },
    {
        id: 4,
        nome: 'Brincos-Foice e Martelo',
        preco: 199.90,
        quantidade: 0,
        img:"https://queissocamarada.com/loja/wp-content/uploads/2018/08/moletom-branco-ursal-costas.jpg"
    },
    {
        id: 5,
        nome: 'Camisa-Orgulho de ser Comunista',
        preco: 29.90,
        quantidade: 0,
        img:"https://ecoms1.com/51315/imgs/big/@v3/1678755854211-foice_martelo-xxilbr.jpg.avif"
    },
    {
        id: 6,
        nome: 'Chaveiro-O fantasma ',
        preco: 99.90,
        quantidade: 0,
        img:"https://ecoms1.com/51315/imgs/big/@v3/1682002614133-256083587_428276985472289_3157863644564957091_n.jpg.avif"
    },
    {
        id: 7,
        nome: 'Poster-Lenin',
        preco: 299.90,
        quantidade: 0,
        img:"https://ecoms1.com/51315/imgs/big/@v3/1679314458079-placa_100.jpg.avif"
    },
    {
        id: 8,
        nome: 'Estatua-Marx',
        preco: 79.90,
        quantidade: 0,
        img:"https://ecoms1.com/51315/imgs/big/@v3/1679431624226-marx04a.jpg.avif"
    },
    {
        id: 9,
        nome: 'Moletom-O fantasma',
        preco: 19.90,
        quantidade: 0,
        img:"https://ecoms1.com/51315/imgs/big/@v3/1679671783950-angela_01.jpg.avif"
    },
    {
        id: 10,
        nome: 'Bandeira',
        preco: 9.90,
        quantidade: 0,
      img:"https://ecoms1.com/51315/imgs/big/@v3/1679433128532-lenin2_02.jpg.avif"  
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

  <div class="carrinho">
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
ul{
  width: 300px;
}
button{
  border-color: rgba(13, 13, 14, 0.605);
}



</style>