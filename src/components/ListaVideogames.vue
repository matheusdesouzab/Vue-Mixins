<template>
    <h3>Lista Videogames</h3>
    <input type="text" placeholder="Nome do jogo" v-model="item">
    <button type="button" @click="adicionarItem()">Adicionar</button>
    <ul>
        <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
    <button type="button" @click="removerItem()">Remover jogo</button>
</template>


<script>
import ListaMixin from '@/mixins/ListaMixin';
import RemoverItem from '@/mixins/RemoverItem';

export default{
    name: 'ListaVideogames',
    mixins: [ListaMixin, RemoverItem]
}
</script>