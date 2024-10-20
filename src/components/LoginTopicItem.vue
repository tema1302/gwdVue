<template>
  <div class="row">
    <div class="col-12 col-md-7" :class="imagePosition === 'right' ? 'order-md-1' : 'order-md-0'">
      <img :src="imageSrc" :alt="imageAlt" class="img-fluid" />
    </div>
    <div class="col-12 col-md-5" :class="imagePosition === 'right' ? 'order-md-0' : 'order-md-1'">
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
      <ul v-if="listItems.length">
        <li v-for="(item, index) in listItems" :key="index">{{ item }}</li>
      </ul>
    </div>

    <div class="col-12 d-none d-md-block order-md-2">
      <hr class="separator" />
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  imageSrc: {
    type: String,
    required: true,
  },
  imageAlt: {
    type: String,
    default: '',
  },
  listItems: {
    type: Array,
    default: () => [],
  },
  imagePosition: {
    type: String,
    default: 'left',
  },
});
</script>
