<template>
    <main>
        <HeaderImage :source="'/1.jpg'" />
        <section class="container">
        <h1>{{title}}</h1>
        <p>
            Lorem ipsun dolor sit, amet bla jfewonfw oidnodiqwndipqnfo fonf. 
        </p>
        </section>
        <section class="container cards-section">
            <article-card 
                v-for="(article, index) in articles"
                :key="index"
                :article="article"
                />
        </section>
    </main>
</template>

<style lang="postcss">
.cards-section{
    display:flex;
    justify-content: space-between;
}
</style>

<script setup>
import { ref } from 'vue'
const title = ref('Homepage')

const articles = ref ([
    {
        id: 1,
        title: "Article 1",
        url: "https://picsum.photos/500/300"
    },
    {
        id: 2,
        title: "Article 2",
        url: "https://picsum.photos/500/301"
    },
    {
        id: 3,
        title: "Article 3",
        url: "https://picsum.photos/500/302"
    },
    {
        id: 4,
        title: "Article 4",
        url: "https://picsum.photos/500/303"
    },
])
</script>

