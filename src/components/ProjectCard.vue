```vue
<script setup>
defineProps({
  project: Object
})
</script>

<template>
  <article class="card">

    <div
      class="project-image"
      :style="{ background: project.color }"
    >
      <span>{{ project.number }}</span>

      <div class="arrow">
        ↗
      </div>
    </div>

    <div class="project-info">
      <span class="category">
        {{ project.category }}
      </span>

      <h3>{{ project.title }}</h3>

      <p>{{ project.description }}</p>
    </div>

  </article>
</template>

<style scoped>
.card {
  cursor: pointer;
}

.project-image {
  position: relative;
  height: 380px;
  padding: 25px;
  transition: .4s;
}

.card:hover .project-image {
  transform: translateY(-8px);
}

.project-image > span {
  color: rgba(40, 35, 33, .5);
  font-family: monospace;
  font-size: 12px;
}

.arrow {
  position: absolute;
  right: 25px;
  bottom: 25px;
  width: 45px;
  height: 45px;
  display: grid;
  place-items: center;
  border-radius: 50%;
  background: rgba(255,255,255,.7);
  font-size: 20px;
}

.project-info {
  padding-top: 20px;
}

.category {
  color: #a57c73;
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 1.5px;
}

h3 {
  margin: 8px 0;
  font-family: 'Playfair Display', serif;
  font-size: 30px;
  font-weight: 400;
}

p {
  margin: 0;
  color: #77706c;
  font-size: 13px;
  line-height: 1.7;
}
</style>
```
