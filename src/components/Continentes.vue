<template>
    <div class="text-center">
        <h3>Filtrar por Continente</h3>
        <div class="btn-group mb-3">
            <button class="btn btn-dark" @click="filtro('Americas')">AMERICA</button>
            <button class="btn btn-dark" @click="filtro('Europe')">EUROPA</button>
            <button class="btn btn-dark" @click="filtro('Asia')">ASIA</button>
            <button class="btn btn-dark" @click="filtro('Oceania')">OCEANIA</button>
            <button class="btn btn-dark" @click="filtro('Africa')">AFRICA</button>
            <button class="btn btn-dark" @click="filtro('')">TODOS</button>
        </div>
    </div>
</template>

<script>
import { useStore } from 'vuex'
export default {
    setup(){
        const store = useStore()

        const filtro = (region) => {
            store.dispatch('filtrarRegion', region)
        }

        return {filtro}
    }
}
</script>