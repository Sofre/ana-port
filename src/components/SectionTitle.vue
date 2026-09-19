```vue
<script setup>
defineProps({
  number: String,
  title: String
})
</script>

<template>
  <div class="title">
    <span>{{ number }} /</span>
    <h2>{{ title }}</h2>
  </div>
</template>

<style scoped>
.title {
  display: flex;
  align-items: baseline;
  gap: 25px;
}

.title span {
  color: #a57c73;
  font-family: monospace;
  font-size: 12px;
}

.title h2 {
  margin: 0;
  font-family: 'Playfair Display', serif;
  font-size: clamp(38px, 5vw, 60px);
  font-weight: 400;
  letter-spacing: -2px;
}
</style>
```
