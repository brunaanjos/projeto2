<script setup>
import { ref } from 'vue'

const leninprodutos = ref([
  {
    id: 1,
    nome: 'Livro Lênin',
    preco: 85.0,
    quantidade: 0,
    imagem: 'https://ecoms1.com/51315/imgs/big/@v3/1682002613642-lenin01.jpg.avif'
  },
  {
    id: 2,
    nome: 'Azulejo Lenin URSS',
    preco: 50.0,
    quantidade: 0,
    imagem: 'https://ecoms1-nyc3.nyc3.cdn.digitaloceanspaces.com/51315/imgs/big/@v3/1678738823446-azulejo03.jpg.webp'
  },
  {
    id: 3,
    nome: 'Estatueta Busto Lenin ',
    preco: 195.0,
    quantidade: 0,
    imagem: 'https://ecoms1.com/51315/imgs/big/@v3/1679491367474-lenin1_01.jpg.avif'
  }
  
])
function incrementar1(id) {
  console.log(leninprodutos.value[id])
  leninprodutos.value[id - 1].quantidade++
}
function decrementar1(id) {
  if (leninprodutos.value[id - 1].quantidade > 0) {
    leninprodutos.value[id - 1].quantidade--
  }
}

function adicionar1(id) {
  if (leninprodutos.value[id - 1].quantidade > 0) {
    carrinho.value.itens.push({
      ...leninprodutos.value[id - 1],
      preco: leninprodutos.value[id - 1].quantidade * leninprodutos.value[id - 1].preco
    })

    calcularTotal()
  }
}
function resetar1(id) {
if (leninprodutos.value[id - 1].quantidade > 0) {
  leninprodutos.value[id - 1].quantidade = 0 }
}
const ursalprodutos = ref([
  {
    id: 1,
    nome: 'Moletom–URSAL',
    preco: 100.0,
    quantidade: 0,
    imagem: 'https://queissocamarada.com/loja/wp-content/webp-express/webp-images/uploads/2018/08/moletom-branco-ursal-costas.jpg.webp'
  },
  {
    id: 2,
    nome: 'Pin Ursal',
    preco: 25.0,
    quantidade: 0,
    imagem: 'https://cf.shopee.com.br/file/272eaab2041b706d99c5fd8bb96e9b38'
  },
  {
    id: 3,
    nome: 'Poster – URSAL',
    preco: 15.0,
    quantidade: 0,
    imagem: 'https://queissocamarada.com/loja/wp-content/uploads/2018/11/Poster_Ursal.png'
  }
])
function incrementar2(id) {
  console.log(ursalprodutos.value[id])
  ursalprodutos.value[id - 1].quantidade++
}
function decrementar2(id) {
  if (ursalprodutos.value[id - 1].quantidade > 0) {
    ursalprodutos.value[id - 1].quantidade--
  }
}

function adicionar2(id) {
  if (ursalprodutos.value[id - 1].quantidade > 0) {
    carrinho.value.itens.push({
      ...ursalprodutos.value[id - 1],
      preco: ursalprodutos.value[id - 1].quantidade * ursalprodutos.value[id - 1].preco
    })

    calcularTotal()
  }
}
function resetar2(id) {
if (ursalprodutos.value[id - 1].quantidade > 0) {
  ursalprodutos.value[id - 1].quantidade = 0 }
}
const marxprodutos = ref([
  {
    id: 1,
    nome: 'Estátua – Karl Marx 3D',
    preco: 200.0,
    quantidade: 0,
    imagem: 'https://queissocamarada.com/loja/wp-content/uploads/2022/01/Marx-M.jpg'
  },
  {
    id: 2,
    nome: 'Moletom com capuz – Karl Marx',
    preco: 159.9,
    quantidade: 0,
    imagem: 'https://queissocamarada.com/loja/wp-content/uploads/2018/10/moletom-branco-marx-1.jpg'
  },
  {
    id: 3,
    nome: 'Body para bebê – Karl Marx',
    preco: 55.0,
    quantidade: 0,
    imagem: 'https://queissocamarada.com/loja/wp-content/uploads/2021/10/Body-verao-Marx-Vermelo.jpg'
  }
])
function incrementar3(id) {
  console.log(marxprodutos.value[id])
  marxprodutos.value[id - 1].quantidade++
}
function decrementar3(id) {
  if (marxprodutos.value[id - 1].quantidade > 0) {
    marxprodutos.value[id - 1].quantidade--
  }
}

function adicionar3(id) {
  if (marxprodutos.value[id - 1].quantidade > 0) {
    carrinho.value.itens.push({
      ...marxprodutos.value[id - 1],
      preco: marxprodutos.value[id - 1].quantidade * marxprodutos.value[id - 1].preco
    })

    calcularTotal()
  }
}
function resetar3(id) {
  if (marxprodutos.value[id - 1].quantidade > 0) {
    marxprodutos.value[id - 1].quantidade = 0 }
}
const porcosprodutos = ref([
  {
    id: 1,
    nome: 'Camiseta–Donald Trump Porco Fascista',
    preco: 49.9,
    quantidade: 0,
    imagem: 'https://queissocamarada.com/loja/wp-content/uploads/2020/01/camiseta-branca-trump.jpg'
  },
  {
    id: 2,
    nome: 'Poster – Tribunal de Haia , Fora Bolsonaro',
    preco: 40.0,
    quantidade: 0,
    imagem: 'https://queissocamarada.com/loja/wp-content/uploads/2021/07/Tribunal-de-Haia-_Poster.jpg'
  },
  {
    id: 3,
    nome: 'Camiseta – Ele não, Ele nunca ',
    preco: 39.9,
    quantidade: 0,
    imagem: 'https://queissocamarada.com/loja/wp-content/uploads/2019/11/camiseta-ele-nao-vermelha-basica.jpg'
  }
  
])
function incrementar4(id) {
  console.log(porcosprodutos.value[id])
  porcosprodutos.value[id - 1].quantidade++
}
function decrementar4(id) {
  if (porcosprodutos.value[id - 1].quantidade > 0) {
    porcosprodutos.value[id - 1].quantidade--
  }
}


function calcularTotal() {
  carrinho.value.total = 0.00;
  for (let item of carrinho.value.itens) {
    carrinho.value.total += item.quantidade * item.preco;
  }
}

function adicionar4(id) {
  if (porcosprodutos.value[id - 1].quantidade > 0) {
    carrinho.value.itens.push({
      ...porcosprodutos.value[id - 1],
      preco: porcosprodutos.value[id - 1].quantidade * porcosprodutos.value[id - 1].preco
    })

    calcularTotal()
  }
}
function resetar4(id) {
  if (porcosprodutos.value[id - 1].quantidade > 0) {
    porcosprodutos.value[id - 1].quantidade = 0 }
}
const carrinho = ref({
  itens: [],
  total: 0
})

const mostrar = ref(false)

function remover(id){
  let item = carrinho.value.itens.findIndex(item => item > id);
  carrinho.value.itens.splice(item, 1);
  calcularTotal()
}

</script>

<template>
  <div id="loja-completa">
    <h1>Communis Store</h1>
    
    <div>
      
    </div>
    <hr>
    <div id="produtos">
      <div id="leninprodutos">
        <h2>Lênin</h2>
        <div class="marcas">
          <div v-for="(produto, index) in leninprodutos" :key="index" class="produto">
            <h4>{{ produto.nome }}</h4>
            <img :src="produto.imagem" alt="" width="200" />
            <div class="informacoes">
              <h3>R${{ produto.preco.toFixed(2) }}</h3>
              <button class="btn-adicionar" @click="incrementar1(produto.id)">+</button>
              <img src="" alt="" width="25" class="btn-deletar" @click="resetar1(produto.id)" />
              <button class="btn-decrmentar" @click="decrementar1(produto.id)">-</button>
              <p>Quantidade de produto(s): {{ produto.quantidade }}</p>
              <button class="btn-adicionar" @click="adicionar1(produto.id)">Adicionar ao Carrinho</button>
            </div>
          </div>
        </div>
      </div>
      <hr />
      <div id="ursalprodutos">
        <h2>URSAL</h2>
        <div class="marcas">
          <div v-for="(produto, index) in ursalprodutos" :key="index" class="produto">
            <h4>{{ produto.nome }}</h4>
            <img :src="produto.imagem" alt="" width="200" />
            <div class="informacoes">
              <h3>R${{ produto.preco.toFixed(2) }}</h3>
              <button class="btn-adicionar" @click="incrementar2(produto.id)">+</button>
              <img src="" alt="" width="25" class="btn-deletar" @click="resetar2(produto.id)" />
              <button class="btn-decrmentar" @click="decrementar2(produto.id)">-</button>
              <p>Quantidade de produto(s): {{ produto.quantidade }}</p>
              <button class="btn-adicionar" @click="adicionar2(produto.id)">Adicionar ao Carrinho</button>
            </div>
          </div>
        </div>
      </div>
      <hr />
      <div id="produtos-Fran">
        <h2>Karl Marx</h2>
        <div class="marcas">
          <div v-for="(produto, index) in marxprodutos" :key="index" class="produto">
            <h4>{{ produto.nome }}</h4>
            <img :src="produto.imagem" alt="" width="200" />
            <div class="informacoes">
              <h3>R${{ produto.preco.toFixed(2) }}</h3>
              <button class="btn-adicionar" @click="incrementar3(produto.id)">+</button>
              <img src="" alt="" width="25" class="btn-deletar" @click="resetar3(produto.id)" />
              <button class="btn-decrmentar" @click="decrementar3(produto.id)">-</button>
              <p>Quantidade de produto(s): {{ produto.quantidade }}</p>
              <button class="btn-adicionar" @click="adicionar3(produto.id)">Adicionar ao Carrinho</button>
            </div>
          </div>
        </div>
      </div>
      <hr />
      <div id="produtos-bocaRosa">
        <h2>Porcos</h2>
        <div class="marcas">
          <div v-for="(produto, index) in porcosprodutos" :key="index" class="produto">
            <h4>{{ produto.nome }}</h4>
            <img :src="produto.imagem" alt="" width="200" />
            <div class="informacoes">
              <h3>R${{ produto.preco.toFixed(2) }}</h3>
              <button class="btn-adicionar" @click="incrementar4(produto.id)">+</button>
              <img src="" alt="" width="25" class="btn-deletar" @click="resetar4(produto.id)" />
              <button class="btn-decrmentar" @click="decrementar4(produto.id)">-</button>
              <p>Quantidade de produto(s): {{ produto.quantidade }}</p>
              <button class="btn-adicionar" @click="adicionar4(produto.id)">Adicionar ao Carrinho</button>
            </div>
          </div>
        </div>
      </div>
      <hr>
    </div>
    <div>
      <button class="btn-carrinho"  @click="mostrar = true"><a href="#carrinho"></a>Carrinho</button>
    </div>
    <div id="carrinho" v-if="mostrar">
     <h2>Carrinho de Compras </h2>
     <button @click="mostrar = false" class="btn-ocultar">Ocultar</button>
     <div id="item-carrinho" v-for="produto in carrinho.itens" :key="produto.id">
      <p>Item: {{ produto.nome }}</p>
      <p>Preco: {{ produto.preco.toFixed(2) }}</p>
      <p>Quantidade: {{ produto.quantidade }}</p>
      <div class="botao"><button @click="remover(produto.id)">Remover</button>
    </div></div>
    <p class="total">Total: R${{ carrinho.total.toFixed(2) }}</p>
  </div>
    </div>
</template>

<style scoped>
.marcas {
  display: flex;
  justify-content: space-between;
  text-align: center;
  flex-direction: row;
  height: 450px;
}

.produto {
  margin: 35px;
}

h1 {
  text-align: center;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  color: rgb(255, 0, 0);
  font-size: 50px;
}
h2 {
  text-align: left;
  color: rgb(255, 0, 0);
  margin: 5px;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
}
p {
  color: rgb(97, 4, 40);
}

img > .btn-deletar {
  box-shadow: none;
}
h4 {
  color: rgb(255, 255, 255);
  text-align: center;
  font-size: 20px;
  margin-bottom: 10px;
}
h3 {
  text-shadow: 5px 5px 10px rgb(0, 0, 0);
  color: rgb(255, 255, 255);
}
button {
  color: white;
  background-color: rgb(158, 0, 0);
  border-color: rgb(255, 0, 0);
  border-style: double;
  border-radius: 5px;
}
button:hover {
  background-color: rgb(227, 0, 0);
  box-shadow: 2px 2px 5px rgba(196, 1, 1, 0.473);
}
hr {
  border-style: solid;
  color: rgb(157, 36, 36);
  margin: 10px;
}
.informacoes{
  position: absolute;
  bottom: 0%;
}
.btn-carrinho{
  font-size:35px;
  background-color: firebrick;
  
  
}
.marcas > img{
  position: absolute;
  bottom: 0%;
}
#carrinho>h2{
  color: rgb(255, 0, 0);
 
}
#carrinho{
  text-align: left;
  font-size: 20px;
}
.total{
  border-radius: 10px;
  font-size: 25px;
  color: rgb(242, 237, 237);
  
}
.btn-ocultar{
  font-size: 15px;
}
a{
  color: rgb(254, 254, 254);
}
p{
  color: rgb(235, 213, 213);
}
.lojacompleta{
  text-align: center;
}
@media screen and (max-width: 1020px) {
  .marcas {
  display: flex;
  justify-content: space-between;
  text-align: center;
  flex-direction: row;
  height: 450px;
}

.produto {
  margin: 35px;
}

h1 {
  text-align: center;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  color: rgb(255, 0, 0);
  font-size: 50px;
}
h2 {
  text-align: left;
  color: rgb(255, 0, 0);
  margin: 5px;
  font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
}
p {
  color: rgb(97, 4, 40);
}

img > .btn-deletar {
  box-shadow: none;
}
h4 {
  color: rgb(255, 255, 255);
  text-align: center;
  font-size: 20px;
  margin-bottom: 10px;
}
h3 {
  text-shadow: 5px 5px 10px rgb(0, 0, 0);
  color: rgb(255, 255, 255);
}
button {
  color: white;
  background-color: rgb(158, 0, 0);
  border-color: rgb(255, 0, 0);
  border-style: double;
  border-radius: 5px;
}
button:hover {
  background-color: rgb(227, 0, 0);
  box-shadow: 2px 2px 5px rgba(196, 1, 1, 0.473);
}
hr {
  border-style: solid;
  color: rgb(157, 36, 36);
  margin: 10px;
}
.informacoes{
  position: absolute;
  bottom: 0%;
}
.btn-carrinho{
  font-size:35px;
  background-color: firebrick;
  
  
}
.marcas > img{
  position: absolute;
  bottom: 0%;
}
#carrinho>h2{
  color: rgb(255, 0, 0);
 
}
#carrinho{
  text-align: left;
  font-size: 20px;
}
.total{
  border-radius: 10px;
  font-size: 25px;
  color: rgb(242, 237, 237);
  
}
.btn-ocultar{
  font-size: 15px;
}
a{
  color: rgb(254, 254, 254);
}
p{
  color: rgb(219, 219, 219);
}
          }
</style>