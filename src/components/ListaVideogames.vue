<template>
    <h4>Lista de Videogames</h4>
    <div class="input-group mb-3">
        <input type="text" class="form-control" placeholder="Nome do jogo" aria-label="Recipient's username"
            aria-describedby="button-addon2" v-model="item">
        <button class="btn btn-outline-success" type="button" id="button-addon2"
            @click="adicionarItem()">Adicionar</button>
    </div>
    <ul class="list-group mb-3">
        <li class="list-group-item" v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
    <button type="button" class="btn btn-danger py-2 px-3" @click="removerItem()">Remover jogo</button>
</template>


<script>
import ListaMixin from '@/mixins/ListaMixin';
import RemoverItem from '@/mixins/RemoverItem';

export default {
    name: 'ListaVideogames',
    mixins: [ListaMixin, RemoverItem]
}
</script>