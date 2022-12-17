<template>
    <h3>Lista Pessoas</h3>
    <input type="text" placeholder="Nome da pessoa" v-model="item">
    <button type="button" @click="adicionarItem()">Adicionar</button>
    <ul>
        <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
    <button type="button" @click="removerItem()">Remover pessoa</button>
</template>


<script>
import ListaMixin from '@/mixins/ListaMixin';
import RemoverItem from '@/mixins/RemoverItem';

export default{
    name: 'ListaPessoas',
    mixins: [ListaMixin, RemoverItem]
}
</script>