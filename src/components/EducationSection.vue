```vue
<template>
  <section class="education-section">

    <div class="section-heading">
      <span class="eyebrow">01 — EDUCATION</span>

      <h2>
        Learning the
        <em>business behind digital.</em>
      </h2>

      <p>
        Building a strong foundation in e-commerce, digital business,
        marketing and the technologies shaping modern online retail.
      </p>
    </div>

    <div class="education-grid">

      <!-- Main Education Card -->
      <article class="education-card featured">

        <div class="card-top">
          <span class="card-number">01</span>

          <span class="status">
            <span class="status-dot"></span>
            CURRENT
          </span>
        </div>

        <div class="card-icon">
          ✦
        </div>

        <span class="date">
          2024 — Present
        </span>

        <h3>
          E-Commerce &
          <br />
          Digital Business
        </h3>

        <p>
          Developing knowledge in digital commerce, online business
          models, digital marketing, consumer behavior, analytics
          and e-commerce strategy.
        </p>

        <div class="tags">
          <span>Digital Commerce</span>
          <span>Marketing</span>
          <span>Analytics</span>
        </div>

        <div class="card-decoration">
          01
        </div>

      </article>

      <!-- Secondary Card -->
      <article class="education-card">

        <div class="card-top">
          <span class="card-number">02</span>

          <span class="mini-label">
            DEVELOPMENT
          </span>
        </div>

        <div class="small-icon">
          ↗
        </div>

        <span class="date">
          Ongoing
        </span>

        <h3>
          Self-Directed
          <br />
          Learning
        </h3>

        <p>
          Expanding my practical skills through personal projects,
          digital design, web technologies and e-commerce experiments.
        </p>

        <div class="tags">
          <span>Vue 3</span>
          <span>Figma</span>
          <span>UX</span>
        </div>

      </article>

    </div>

  </section>
</template>

<style scoped>
.education-section {
  padding: 140px 0;
}

.section-heading {
  max-width: 760px;
  margin-bottom: 70px;
}

.eyebrow {
  display: block;

  margin-bottom: 22px;

  color: #a57c73;

  font-size: 11px;
  font-weight: 600;

  letter-spacing: 2px;
}

.section-heading h2 {
  margin: 0;

  font-family: 'Playfair Display', serif;

  font-size: clamp(42px, 6vw, 76px);

  font-weight: 400;

  line-height: 1.05;

  letter-spacing: -2px;
}

.section-heading h2 em {
  color: #a57c73;
}

.section-heading p {
  max-width: 550px;

  margin-top: 25px;

  color: #77706c;

  font-size: 15px;

  line-height: 1.8;
}

/* GRID */

.education-grid {
  display: grid;

  grid-template-columns: 1.25fr .75fr;

  gap: 24px;
}

/* CARDS */

.education-card {
  position: relative;

  min-height: 430px;

  padding: 35px;

  overflow: hidden;

  background: #eee8e3;

  border: 1px solid rgba(130, 105, 95, .12);

  transition:
    transform .4s ease,
    box-shadow .4s ease;
}

.education-card:hover {
  transform: translateY(-8px);

  box-shadow:
    0 25px 60px rgba(70, 50, 45, .12);
}

.education-card.featured {
  background:
    linear-gradient(
      135deg,
      #292625 0%,
      #3b3330 60%,
      #544541 100%
    );

  color: white;
}

/* TOP */

.card-top {
  display: flex;

  align-items: center;

  justify-content: space-between;
}

.card-number {
  font-family: 'Playfair Display', serif;

  font-size: 20px;

  color: #a57c73;
}

.featured .card-number {
  color: #d8a99c;
}

.status,
.mini-label {
  font-size: 9px;

  letter-spacing: 1.8px;
}

.status {
  display: flex;

  align-items: center;

  gap: 7px;

  color: #d8a99c;
}

.status-dot {
  width: 6px;
  height: 6px;

  border-radius: 50%;

  background: #d8a99c;

  box-shadow:
    0 0 0 4px rgba(216,169,156,.1);
}

/* ICONS */

.card-icon {
  width: 58px;
  height: 58px;

  display: flex;

  align-items: center;
  justify-content: center;

  margin-top: 55px;

  border-radius: 50%;

  background: #d8a99c;

  color: #292625;

  font-size: 25px;
}

.small-icon {
  width: 48px;
  height: 48px;

  display: flex;

  align-items: center;
  justify-content: center;

  margin-top: 55px;

  border-radius: 50%;

  background: #292625;

  color: white;

  font-size: 18px;
}

/* CONTENT */

.date {
  display: block;

  margin-top: 28px;

  color: #a57c73;

  font-size: 11px;

  letter-spacing: 1px;

  text-transform: uppercase;
}

.featured .date {
  color: #d8a99c;
}

.education-card h3 {
  margin: 12px 0 18px;

  font-family: 'Playfair Display', serif;

  font-size: clamp(30px, 4vw, 45px);

  font-weight: 400;

  line-height: 1.05;
}

.education-card p {
  max-width: 560px;

  color: #756e6a;

  font-size: 14px;

  line-height: 1.8;
}

.featured p {
  color: #c9bfbb;
}

/* TAGS */

.tags {
  display: flex;

  flex-wrap: wrap;

  gap: 8px;

  margin-top: 28px;
}

.tags span {
  padding: 7px 11px;

  border: 1px solid #d1c4be;

  color: #756e6a;

  font-size: 10px;
}

.featured .tags span {
  border-color: rgba(255,255,255,.18);

  color: #d9cfcb;
}

/* DECORATION */

.card-decoration {
  position: absolute;

  right: -20px;
  bottom: -55px;

  font-family: 'Playfair Display', serif;

  font-size: 180px;

  line-height: 1;

  color: rgba(255,255,255,.035);

  pointer-events: none;
}

@media (max-width: 800px) {
  .education-grid {
    grid-template-columns: 1fr;
  }

  .education-card {
    min-height: 400px;
  }
}

@media (max-width: 500px) {
  .education-section {
    padding: 90px 0;
  }

  .education-card {
    padding: 28px;

    min-height: 380px;
  }
}
</style>
```
