<script setup lang="ts">
import { onMounted, ref } from "vue";
import { gsap } from "gsap";

const marquee = ref<HTMLElement | null>(null);

function animate(el: HTMLElement) {
  gsap.to(el, {
    duration: 2,
    background: 'linear-gradient(45deg, #FF6A00, #EE0979)',
    ease: "power4.out",
    repeat: -1,
    yoyo: true,
  });
}

onMounted(() => {
  const marqueeElement = marquee.value;
  animate(marqueeElement as HTMLElement);
});
</script>
<template>
  <div class="marquee" ref="marquee">
    <h1 class="marquee__text">BAKEN667&BAUKAAA&BAKE&</h1>
    <h1 class="marquee__text">BAKEN667&BAUKAAA&BAKE&</h1>
  </div>
</template>
