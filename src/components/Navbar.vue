```vue
<template>
  <header class="navbar">
    <a href="#" class="logo">ANA<span>.</span></a>

    <nav>
      <a href="#about">About</a>
      <a href="#work">Work</a>
      <a href="#skills">Skills</a>
      <a href="#education">Education</a>
      <a href="#contact">Contact</a>
    </nav>

    <a href="#contact" class="availability">
      <span></span>
      Available 24/7
    </a>
  </header>
</template>

<style scoped>
.navbar {
  height: 90px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid #dfd9d4;
}

.logo {
  font-family: 'Playfair Display', serif;
  font-size: 27px;
  letter-spacing: 2px;
}

.logo span {
  color: #a57c73;
}

nav {
  display: flex;
  gap: 40px;
}

nav a {
  color: #706966;
  font-size: 13px;
  transition: .2s;
}

nav a:hover {
  color: #292625;
}

.availability {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 11px;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.availability span {
  width: 7px;
  height: 7px;
  background: #22C003;
  border-radius: 50%;
}

@media (max-width: 600px) {
  nav {
    display: none;
  }
}
</style>
```
