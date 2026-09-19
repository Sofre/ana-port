```vue
<script setup>
defineProps({
  name: String
})
</script>

<template>
  <div class="pill">
    <span>✦</span>
    {{ name }}
  </div>
</template>

<style scoped>
.pill {
  padding: 14px 20px;
  border: 1px solid #d8cec8;
  border-radius: 100px;
  color: #625b57;
  font-size: 13px;
  transition: .3s;
}

.pill span {
  margin-right: 8px;
  color: #b18b82;
}

.pill:hover {
  background: #292625;
  color: white;
  border-color: #292625;
  transform: translateY(-3px);
}
</style>
```
