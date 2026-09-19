```vue
<script setup lang="ts">
import anaPhoto from '../assets/ana.png'
defineProps<{
  src: string
  alt?: string
  linkedin?: string
}>()
</script>

<template>
  <div class="profile-wrapper">

    <div class="portrait-frame">
      <img
        :src="anaPhoto"
        :alt="alt || 'Profile photo'"
        class="profile-image"
      />

      <div class="photo-decoration">
        ✦
      </div>
    </div>

    <!-- LinkedIn headline -->
    <div class="linkedin-card">

      <div class="linkedin-icon">
        in
      </div>

      <div class="linkedin-content">

        <span class="linkedin-label">
          LINKEDIN
        </span>

        <h3>
          E-Commerce Student
        </h3>

        <p>
          Digital Business · E-Commerce · Marketing
        </p>

      </div>

      <a
        :href="linkedin || '#'"
        target="_blank"
        rel="noopener noreferrer"
        class="linkedin-arrow"
        aria-label="Visit my LinkedIn"
      >
        ↗
      </a>

    </div>

  </div>
</template>

<style scoped>
.profile-wrapper {
  width: 100%;
  max-width: 410px;

  display: flex;
  flex-direction: column;
  align-items: center;
}

/* PHOTO */

.portrait-frame {
  position: relative;

  width: 390px;
  height: 500px;

  padding: 14px;

  background: #e8ddd8;

  transform: rotate(2deg);

  box-shadow:
    0 25px 60px rgba(60, 45, 40, .12);

  transition:
    transform .4s ease,
    box-shadow .4s ease;
}

.portrait-frame:hover {
  transform:
    rotate(0deg)
    translateY(-6px);

  box-shadow:
    0 35px 70px rgba(60, 45, 40, .18);
}

.profile-image {
  width: 100%;
  height: 100%;

  display: block;

  object-fit: cover;

  background:
    linear-gradient(
      135deg,
      #d6c0b9,
      #eee5df
    );
}

.photo-decoration {
  position: absolute;

  top: -18px;
  right: -18px;

  width: 55px;
  height: 55px;

  display: flex;

  align-items: center;
  justify-content: center;

  border-radius: 50%;

  background: #292625;

  color: #d8a99c;

  font-size: 23px;

  box-shadow:
    0 12px 30px rgba(0,0,0,.12);
}


/* LINKEDIN CARD */

.linkedin-card {
  position: relative;

  z-index: 2;

  width: 92%;

  display: flex;

  align-items: center;

  gap: 14px;

  margin-top: -10px;

  padding: 17px 18px;

  background: #292625;

  color: white;

  box-shadow:
    0 18px 45px rgba(40,35,33,.18);

  transition:
    transform .3s ease,
    background .3s ease;
}

.linkedin-card:hover {
  transform:
    translateY(-4px);

  background: #332e2c;
}


/* LINKEDIN ICON */

.linkedin-icon {
  width: 38px;
  height: 38px;

  flex-shrink: 0;

  display: flex;

  align-items: center;
  justify-content: center;

  border-radius: 7px;

  background: #0a66c2;

  color: white;

  font-family:
    Arial,
    sans-serif;

  font-size: 19px;

  font-weight: 700;
}


/* TEXT */

.linkedin-content {
  min-width: 0;

  flex: 1;
}

.linkedin-label {
  display: block;

  margin-bottom: 3px;

  color: #d8a99c;

  font-size: 8px;

  font-weight: 600;

  letter-spacing: 1.8px;
}

.linkedin-content h3 {
  margin: 0;

  font-family:
    'DM Sans',
    sans-serif;

  font-size: 13px;

  font-weight: 600;
}

.linkedin-content p {
  margin: 4px 0 0;

  overflow: hidden;

  color: #aaa19d;

  font-size: 10px;

  line-height: 1.4;

  white-space: nowrap;

  text-overflow: ellipsis;
}


/* ARROW */

.linkedin-arrow {
  width: 34px;
  height: 34px;

  flex-shrink: 0;

  display: flex;

  align-items: center;
  justify-content: center;

  border:
    1px solid rgba(255,255,255,.15);

  color: white;

  font-size: 16px;

  transition:
    transform .3s ease,
    background .3s ease;
}

.linkedin-arrow:hover {
  background: #a57c73;

  transform:
    rotate(45deg);
}


/* MOBILE */

@media (max-width: 600px) {

  .profile-wrapper {
    max-width: 320px;
  }

  .portrait-frame {
    width: 290px;
    height: 380px;
  }

  .linkedin-card {
    width: 95%;

    padding: 14px;
  }

  .linkedin-content h3 {
    font-size: 12px;
  }

  .linkedin-content p {
    font-size: 9px;
  }
}
</style>
```
