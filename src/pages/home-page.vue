<script lang="ts" setup>
import { ref } from 'vue';

import HeroLeft from '../components/heros/hero-left.vue';

import TeacherHero from '@images/teacher-hero.jpg';
import StudentHero from '@images/student-hero.jpg';

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

    <hero-left
        title="For Teachers"
        :img-src="TeacherHero"
        img-alt=""
        Teacher
        teaching
        class
    >
        Manage class activities, classrooms and many other features in the
        teachers portal.
    </hero-left>

    <hero-left
        title="For Students"
        :img-src="StudentHero"
        img-alt="Student taking class"
    >
        Participate in activities in the students portal.
    </hero-left>
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
