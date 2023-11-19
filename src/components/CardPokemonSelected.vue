<script setup>
const pokemon = defineProps(["name", "xp", "height", "image", "loading"])
</script>
<template>
    <div class="card cardPokemonSelected" :class="loading ? '' : 'animate__animated animate__flipInY'">
        <img v-if="pokemon.name" :src="pokemon.image" class="card-img-top pt-2" height="250" :alt="pokemon.name">
        <img v-else src="../assets/pokeball.svg" class="card-img-top pt-2" height="250" :alt="pokemon.name">
        <div class="card-body">
            <h4 class="card-title text-center">{{ pokemon.name || '???' }}</h4>
            <hr>
            <div class="row">
                <section class="col">
                    <strong>XP:</strong>
                    <span>{{ pokemon.xp }}</span>
                </section>
                <section class="col">
                    <strong>Altura:</strong>
                    <span>{{ pokemon.height/10 }}</span>
                </section>
            </div>
        </div>
    </div>
</template>
<style scoped>
.cardPokemonSelected {
    border: none;
    box-shadow: 6px 6px 5px 0px rgba(0,0,0,0.3);
    height: 75vh;
    background: rgb(238, 174, 202);
    background: linear-gradient(0deg, rgba(238, 174, 202, 1) 0%, rgba(148, 187, 233, 1) 100%);
}
</style>