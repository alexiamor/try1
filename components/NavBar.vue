<template>
    <nav>
        <ul>
            <li>
                <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/about">About</NuxtLink>
            </li>
        </ul>
        <div 
        class="user"
        @click="panelActive = !panelActive">miau</div>
        <div 
        class="panel"
        v-show="panelActive">
    </div>
    </nav>
</template>

<script setup>
import {ref} from 'vue'
const panelActive = ref(false)
</script>

<style lang="postcss">
ul {
    @apply flex p-4;

    li {
        @apply p-4;
    }
}

.panel{
    height: 1rem;
    width:1rem;
    background-color: cornflowerblue;
}
</style>