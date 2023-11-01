<script setup>
const pokemon = defineProps(["name", "urlBaseSvg"])
</script>

<template>
    <div class="col-4">
        <div class="card p-2 mb-3 cardListPokemon">
            <p class="text-center">{{ pokemon.name }}</p>
            <img :src="urlBaseSvg" class="card-img-top" alt="..." height="80" />
        </div>
    </div>
</template>

<style scoped>
.cardListPokemon {
    border: none;
    box-shadow: 2px 2px 3px 0px rgba(0,0,0,0.3);
    background: rgb(34, 44, 195);
    background: linear-gradient(0deg, rgba(70, 78, 197, 0.598) 0%, rgb(120, 233, 208) 100%);
    cursor: pointer;
}
.cardListPokemon:hover {
    background: rgb(34, 44, 195);
    background: linear-gradient(0deg, rgba(46, 56, 197, 0.598) 0%, rgb(69, 231, 196) 100%);
}
.cardListPokemon img:hover {
    padding: .1rem;
}
</style>