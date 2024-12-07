<script setup lang="ts">
import { ref } from 'vue';

const data = ref([
  {
    title: 'Slide Title 1',
    content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut id nunc at ligula bibendum commodo.",
    author: "Andrew"
  },
  {
    title: 'Slide Title 2',
    content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut id nunc at ligula bibendum commodo.",
    author: "Andrew"
  },
  {
    title: 'Slide Title 3',
    content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut id nunc at ligula bibendum commodo.",
    author: "Andrew"
  },
  {
    title: 'Slide Title 4',
    content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut id nunc at ligula bibendum commodo.",
    author: "Andrew"
  },
  {
    title: 'Slide Title 5',
    content: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut id nunc at ligula bibendum commodo.",
    author: "Andrew"
  }
]);
</script>

<template>
  <div class="carousel">
    <div class="fading-left"></div>
    <div class="slide-warpper">
      <div class="slide" v-for="review in data">
        <div class="slide-body">
          <h2 class="slide-title">{{ review.title }}</h2>
          <p class="slide-content">{{ review.content }}</p>
        </div>
        <div class="slide-author">{{ review.author }}</div>
      </div>
      <div class="slide" v-for="review in data">
        <div class="slide-body">
          <h2 class="slide-title">{{ review.title }}</h2>
          <p class="slide-content">{{ review.content }}</p>
        </div>
        <div class="slide-author">{{ review.author }}</div>
      </div>
    </div>
    <div class="fading-right"></div>
  </div>
</template>

<style scoped>
.carousel {
  overflow-x: hidden;
  position: relative;
}

.slide-warpper {
  width: max-content;
  margin-left: 20px;
  display: flex;
  animation: 30s slide-looping linear backwards;
  animation-iteration-count: infinite;
  gap: 16px;
}

@keyframes slide-looping {
  0% {
    transform: translateX(0%);
  }

  100% {
    transform: translateX(-50%);
  }
}

.slide {
  padding: 24px;
  width: 70vw;
  background: #ffffff;
  border-radius: 8px;
}

.fading-left,
.fading-right {
  z-index: 100;
  padding: 20px;
  height: 100%;
  position: absolute;
  top: 0;
}

.fading-left {
  left: 0;
  background: linear-gradient(90deg, var(--color-background) 40%, transparent 90%);
}

.fading-right {
  right: 0;
  background: linear-gradient(270deg, var(--color-background) 40%, transparent 90%);
}
</style>