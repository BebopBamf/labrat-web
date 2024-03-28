<script setup lang="ts">
import { ref } from 'vue';

// Reactive state
const count = ref<number>(0);

// Methods
const increment = () => {
    count.value++;
};

const decrement = () => {
    count.value--;
};
</script>

<template>
    <div class="home">
        <h1>Welcome to the Home Page!</h1>
        <p>This is a simple Vue 3 + TypeScript example.</p>
        <div>
            <button @click="decrement">-</button>
            <span>{{ count }}</span>
            <button @click="increment">+</button>
        </div>
    </div>
</template>

<style scoped>
/* Add your styles here */
.home {
    text-align: center;
    margin-top: 50px;
}

button {
    margin: 0 10px;
}
</style>
