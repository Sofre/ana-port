```vue
<template>
  <div class="cta">

    <span class="small">FEELING INTRESTED?</span>

    <h2>
      People first.
      <em>Results always.</em>
    </h2>

    <a href="mailto:hello@example.com">
      hello@example.com
      <span>↗</span>
    </a>

  </div>
</template>

<style scoped>
.cta {
  padding: 100px 30px;
  background: #e9ddd8;
}

.small {
  color: #8d6d65;
  font-size: 10px;
  letter-spacing: 2px;
}

h2 {
  max-width: 800px;
  margin: 25px auto 45px;
  font-family: 'Playfair Display', serif;
  font-size: clamp(45px, 7vw, 85px);
  line-height: 1;
  font-weight: 400;
  letter-spacing: -3px;
}

h2 em {
  color: #a57c73;
}

a {
  display: inline-flex;
  gap: 15px;
  padding-bottom: 8px;
  border-bottom: 1px solid #292625;
  font-size: 14px;
}

a span {
  color: #a57c73;
}
</style>
```
