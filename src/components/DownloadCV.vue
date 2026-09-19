```vue
<template>
  <a
    class="download-cv"
    href="/Ana-Stojanova-CV.pdf"
    download
  >
    <span class="download-icon">↓</span>

    <span class="download-content">
      <span class="download-label">
        Download CV
      </span>

      <span class="download-subtitle">
        PDF · Curriculum Vitae
      </span>
    </span>

    <span class="download-arrow">
      ↗
    </span>
  </a>
</template>

<style scoped>
.download-cv {
  display: inline-flex;
  align-items: center;
  gap: 14px;

  width: fit-content;
  margin-top: 28px;
  padding: 14px 18px;

  background: #eee8e3;
  border: 1px solid #d9cec8;

  color: #292625;

  text-decoration: none;

  transition:
    transform .3s ease,
    background .3s ease,
    box-shadow .3s ease;
}

.download-cv:hover {
  transform: translateY(-4px);

  background: #292625;
  color: white;

  box-shadow:
    0 15px 35px rgba(70, 50, 45, .15);
}

.download-icon {
  display: flex;
  align-items: center;
  justify-content: center;

  width: 38px;
  height: 38px;

  border-radius: 50%;

  background: #a57c73;
  color: white;

  font-size: 18px;
}

.download-content {
  display: flex;
  flex-direction: column;
  gap: 3px;
}

.download-label {
  font-size: 13px;
  font-weight: 600;
  letter-spacing: .2px;
}

.download-subtitle {
  color: #817873;

  font-size: 9px;
  letter-spacing: 1.2px;
  text-transform: uppercase;
}

.download-cv:hover .download-subtitle {
  color: #c9bfbb;
}

.download-arrow {
  margin-left: 10px;

  font-size: 17px;

  transition: transform .3s ease;
}

.download-cv:hover .download-arrow {
  transform: rotate(45deg);
}

@media (max-width: 600px) {
  .download-cv {
    width: 100%;
    justify-content: center;
  }
}
</style>
