<script setup>
import { livros } from '@/_data/livros.js'
import MeuCarrinho from '@/components/MeuCarrinho.vue';
import CardLivro from '@/components/CardLivro.vue';
</script>

<template>
  <h1>Minha livraria</h1>
  <div class="container-geral">
    <div class="listagem-livros">
      <CardLivro v-for="livro in livros" :key="livro.id" :livro="livro"/>
    </div>
    <MeuCarrinho/>
  </div>
</template>

<style scoped>
.wrap-carrinho .carrinho-total {
  position: fixed;
  bottom: 3%;
  font-size: 1.5rem;
  font-weight: bold;
}

.item-carrinho .info-livro {
  display: flex;
  margin-bottom: 10px;
}
.detalhes-livro {
  display: flex;
  flex-direction: column;
  width: 100%;
}
.detalhes-livro p {
  margin: 0;
}
.detalhes-livro div {
  display: flex;
  justify-content: space-between;
  width: 100%;
}

.detalhes-livro input[type='number'] {
  width: 50px;
  text-align: start;
  border: none;
  margin-left: 10px;
}

.detalhes-livro button {
  background-color: transparent;
  border: none;
  cursor: pointer;
  font-size: 1.5rem;
  color: black;
  padding: 0;
  margin: 0;
}

.info-livro-preco {
  margin-left: auto;
}
.icon-capa-livro {
  width: 30px;
  margin-right: 10px;
}
.container-geral {
  /* display: flex;
  justify-content: space-between; */
  display: grid;
  grid-template-columns: 3fr 1fr;
}

.listagem-livros {
  display: flex;
  flex-wrap: wrap;
}


</style>
