```vue
<script setup lang="ts">
import Navbar from '../components/Navbar.vue'
import HeroBadge from '../components/HeroBadge.vue'
import ProfilePhoto from '../components/ProfilePhoto.vue'
import ProjectCard from '../components/ProjectCard.vue'
import SkillPill from '../components/SkillPill.vue'
import SectionTitle from '../components/SectionTitle.vue'
import ContactCTA from '../components/ContactCTA.vue'
import DownloadCV from '../components/DownloadCV.vue'

const skills = [
'Sales & Customer',
'Communication',
'Microsoft Office',
'Problem Solving',
'Teamwork & Collaboration',
]

const projects = [
  {
    number: '01',
    title: 'Digital Halo Project',
    description:
      'Crafting a winning marketing strategy for attracting new customers and building new services.',
    color: '#e9d8d2'
  },
  {
    number: '02',
    title: 'Hackathon: From Concept to Market',
    description:
      'A 2025 hackathon project focused on developing an idea from concept through market-oriented thinking and presentation.',
    color: '#dce4dc'
  }
]

const experiences = [
  {
    number: '01',
    date: '2023 — 2026',
    type: 'Inditex — Stradivarius',
    title: 'General Sales Assistant',
    description:
      'Achieved monthly sales targets and contributed to store sales objectives. Developed strong problem-solving and people-management skills while working in a fast-paced retail environment.',
    tags: [
      'Sales',
      'Customer Communication',
      'Teamwork'
    ],
    color: 'rose'
  }
  
]

const education = {
  university:
    'Ss. Cyril and Methodius University – Faculty of Economics, Skopje',
  degree: "Bachelor's Degree in Marketing",
  date: '2021 — 2026',
  status: 'All exams completed',
  thesis: "Bachelor's thesis in progress"
}

const courses = [
  {
    number: '01',
    title: 'Introduction to Human Resource Management (HRM)',
    provider: 'Alison',
    date: 'Completed: 2026',
    description:
      'Completed an introductory course covering key principles and practices of human resource management.'
  }
]

const languages = [
  'Macedonian',
  'English',
  'Serbian'
]
</script>

<template>
  <div class="page">

    <Navbar />

    <!-- =========================
         HERO
    ========================== -->

    <section class="hero">

      <div class="hero-copy">

        <HeroBadge />

        <span class="hero-role">
          MARKETING STUDENT · SALES EXPERIENCE
        </span>

        <h1>
          About
          <em>me</em>
        </h1>

        <p class="hero-description">
          I'm Ana, a Marketing student with 3 years of experience
          in sales at Inditex — Stradivarius. I’m passionate about people, communication, 
          and creating meaningful connections.
        </p>

        <div class="hero-actions">

          <a
            href="#work"
            class="button primary"
          >
            Explore my work
            <span>↗</span>
          </a>

          <a
            href="#experience"
            class="button primary"
          >
            View my experience
            <span>↗</span>
          </a>

          <a
            href="#contact"
            class="button text"
          >
            Let's connect
          </a>

        </div>

        <!-- DOWNLOAD CV -->
        <DownloadCV />

        <div class="hero-meta">

          <div>
            <strong>Education</strong>
            <span>Marketing · Faculty of Economics</span>
          </div>

          <div>
            <strong>Experience</strong>
            <span>3 years · Inditex — Stradivarius</span>
          </div>

        </div>

      </div>


      <!-- PHOTO + LINKEDIN -->

      <div class="hero-visual">

        <ProfilePhoto
          src="/profile.jpg"
          alt="Ana Stojanova - Marketing Student"
          linkedin="https://www.linkedin.com/in/your-username/"
        />

      </div>

    </section>


    <!-- =========================
         ABOUT
    ========================== -->

    <section
      id="about"
      class="about section"
    >

      <SectionTitle
        number="01"
        title="A little about me"
      />

      <div class="about-content">

        <div class="about-large">

          <p>
            I believe successful
            <i>organizations</i>
            are built by reconginizing <i>talent,understanding people</i>
            and creating the <i>right connections</i>
          </p>

        </div>

        <div class="about-copy">

          <p>
            I'm currently completing my Bachelor's Degree in
            Marketing at Ss. Cyril and Methodius University –
            Faculty of Economics in Skopje. I have completed
            all my exams and am currently working on my
            Bachelor's thesis.
          </p>

          <p>
            Alongside my studies, I have gained three years of
            practical sales experience at Inditex — Stradivarius.
            This experience helped me develop strong communication,
            customer service, teamwork and problem-solving skills.
          </p>

          <p>
            I'm now looking to gain further practical experience
            in Sales and Marketing and apply what I've learned
            through both my studies and professional experience.
          </p>

          <a
            href="#contact"
            class="underlined-link"
          >
            Let's work together →
          </a>

        </div>

      </div>

    </section>


    <!-- =========================
         EXPERTISE
    ========================== -->

    <section class="skills section">

      <SectionTitle
        number="02"
        title="My expertise"
      />

      <div class="skill-list">

        <SkillPill
          v-for="skill in skills"
          :key="skill"
          :name="skill"
        />

      </div>

    </section>


    <!-- =========================
         EDUCATION
    ========================== -->

    <section
      id="education"
      class="education-section"
    >

      <div class="section-heading">

        <span class="eyebrow">
          03 — EDUCATION
        </span>

        <h2>
          Building the
          <em>foundation.</em>
        </h2>

        <p>
          Developing a strong foundation in marketing, business,
          consumer behavior and communication while combining
          academic knowledge with practical sales experience.
        </p>

      </div>


      <div class="education-grid">

        <!-- UNIVERSITY -->

        <article class="education-card featured">

          <div class="card-top">

            <span class="card-number">
              01
            </span>

            <span class="status">
              <span class="status-dot"></span>
              THESIS IN PROGRESS
            </span>

          </div>

          <div class="card-icon">
            ✦
          </div>

          <span class="date">
            {{ education.date }}
          </span>

          <h3>
            Bachelor's Degree
            <br />
            in Marketing
          </h3>

          <p>
            {{ education.university }}
          </p>

          <div class="education-status">

            <span>
              ✓ {{ education.status }}
            </span>

            <span>
              ✓ {{ education.thesis }}
            </span>

          </div>

          <div class="tags">

            <span>
              Marketing
            </span>

            <span>
              Economics
            </span>

            <span>
              Business
            </span>

          </div>

          <div class="card-decoration">
            01
          </div>

        </article>


        <!-- COURSE -->

        <article
          v-for="course in courses"
          :key="course.number"
          class="education-card course-card"
        >

          <div class="card-top">

            <span class="card-number">
              {{ course.number }}
            </span>

            <span class="mini-label">
              COURSE
            </span>

          </div>

          <div class="small-icon">
            ↗
          </div>

          <span class="date">
            {{ course.date }}
          </span>

          <h3>
            Introduction to
            <br />
            HR Management
          </h3>

          <p>
            {{ course.description }}
          </p>

          <div class="course-provider">
            <span>Provider</span>
            <strong>{{ course.provider }}</strong>
          </div>

        </article>

      </div>

    </section>


    <!-- =========================
         WORK EXPERIENCE
    ========================== -->

    <section
      id="experience"
      class="experience-section"
    >

      <div class="heading-row">

        <div>

          <span class="eyebrow">
            04 — EXPERIENCE
          </span>

          <h2>
            Three years of
            <em>real experience.</em>
          </h2>

        </div>

        <p>
          My experience at Inditex — Stradivarius has helped me
          develop practical sales, communication, customer
          service and teamwork skills in a fast-paced environment.
        </p>

      </div>


      <div class="experience-list">

        <article
          v-for="experience in experiences"
          :key="experience.number"
          class="experience-card"
          :class="experience.color"
        >

          <div class="experience-number">
            {{ experience.number }}
          </div>

          <div class="experience-main">

            <div class="experience-meta">

              <span>
                {{ experience.date }}
              </span>

              <span>•</span>

              <span>
                {{ experience.type }}
              </span>

            </div>

            <h3>
              {{ experience.title }}
            </h3>

            <p>
              {{ experience.description }}
            </p>

            <div class="experience-tags">

              <span
                v-for="tag in experience.tags"
                :key="tag"
              >
                {{ tag }}
              </span>

            </div>

          </div>

          <!--
            PUT YOUR EXPERIENCE LINK HERE:
            Replace # with your desired URL.
          -->

          <a
            href="#"
            class="arrow"
            aria-label="View experience"
          >
            ↗
          </a>

        </article>

      </div>

    </section>


    <!-- =========================
         PROJECTS
    ========================== -->

    <section
      id="work"
      class="work section"
    >

      <SectionTitle
        number="05"
        title="Selected projects"
      />

      <div class="projects">

        <ProjectCard
          v-for="project in projects"
          :key="project.number"
          :project="project"
        />

      </div>

    </section>


    <!-- =========================
         LANGUAGES
    ========================== -->

    <section class="languages-section">

      <div class="languages-heading">

        <span class="eyebrow">
          06 — LANGUAGES
        </span>

        <h2>
          Communication
          <em>across cultures.</em>
        </h2>

      </div>

      <div class="language-grid">

        <div
          v-for="(language, index) in languages"
          :key="language"
          class="language-card"
        >

          <span>
            0{{ index + 1 }}
          </span>

          <strong>
            {{ language }}
          </strong>

          <i>
            ✦
          </i>

        </div>

      </div>

    </section>


    <!-- =========================
         CONTACT
    ========================== -->

    <section
      id="contact"
      class="contact section"
    >

      <ContactCTA />

    </section>


    <!-- =========================
         FOOTER
    ========================== -->

    <footer>

      <span>
        © 2026 Offical Portfolio of Ana Stojanova
      </span>

      <div class="footer-links">

       
        <p>Number : +389 79 369 061</p>
       

      </div>

      <span>
        ✦✦✦✦✦✦✦✦✦✦✦✦✦✦✦✦✦✦✦✦✦✦✦
      </span>

    </footer>

  </div>
</template>


<style scoped>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600&family=Playfair+Display:ital,wght@0,400;0,500;1,400;1,500&display=swap');

:global(*) {
  box-sizing: border-box;
}

:global(html) {
  scroll-behavior: smooth;
}

:global(body) {
  margin: 0;

  background: #f8f5f1;

  color: #292625;

  font-family:
    'DM Sans',
    sans-serif;
}

:global(a) {
  color: inherit;
  text-decoration: none;
}

.page {
  max-width: 1280px;

  margin: auto;

  padding: 0 45px;
}


/* =========================
   HERO
========================= */

.hero {
  min-height: 780px;

  display: grid;

  grid-template-columns:
    1.1fr
    .9fr;

  align-items: center;

  gap: 80px;

  padding: 90px 0;
}

.hero-copy {
  padding-left: 40px;
}

.hero-role {
  display: block;

  margin-top: 30px;

  color: #a57c73;

  font-size: 10px;

  font-weight: 600;

  letter-spacing: 2px;
}

.hero h1 {
  max-width: 760px;

  margin: 20px 0 28px;

  font-size:
    clamp(58px, 7vw, 100px);

  font-weight: 500;

  line-height: .98;

  letter-spacing: -4px;
}

.hero h1 em {
  display: block;

  color: #a57c73;

  font-family:
    'Playfair Display',
    serif;

  font-weight: 400;
}

.hero-description {
  max-width: 570px;

  color: #77706c;

  font-size: 17px;

  line-height: 1.8;
}


/* =========================
   ACTIONS
========================= */

.hero-actions {
  display: flex;

  align-items: center;

  flex-wrap: wrap;

  gap: 18px;

  margin-top: 40px;
}

.button {
  display: inline-flex;

  align-items: center;

  gap: 15px;

  font-size: 14px;
}

.button.primary {
  padding: 16px 24px;

  background: #292625;

  color: white;

  transition:
    .3s ease;
}

.button.primary:hover {
  background: #a57c73;

  transform:
    translateY(-3px);
}

.button.text {
  color: #6f6763;
}

.button.text:hover {
  color: #a57c73;
}


/* =========================
   HERO META
========================= */

.hero-meta {
  display: flex;

  gap: 55px;

  margin-top: 35px;
}

.hero-meta div {
  display: flex;

  flex-direction: column;

  gap: 5px;
}

.hero-meta strong {
  color: #a57c73;

  font-size: 11px;

  text-transform: uppercase;

  letter-spacing: 1.5px;
}

.hero-meta span {
  color: #817873;

  font-size: 12px;
}


/* =========================
   VISUAL
========================= */

.hero-visual {
  position: relative;

  display: flex;

  justify-content: center;

  align-items: center;
}


/* =========================
   SECTIONS
========================= */

.section {
  padding: 140px 0;

  border-top:
    1px solid #dfd9d4;
}


/* =========================
   ABOUT
========================= */

.about-content {
  display: flex;
  flex-direction: column;
  gap: 35px;
  margin-top: 70px;
}


.about-large {
  max-width: 800px;
  font-family: 'Playfair Display', serif;
  font-size: clamp(40px, 5vw, 68px);
  line-height: 1.05;
}

.about-large i {
  color: #a57c73;
}

.about-copy {
  max-width: 650px;
  color: #756e6a;
  font-size: 16px;
  line-height: 1.9;
}

.about-copy p + p {
  margin-top: 25px;
}

.underlined-link {
  display: inline-block;

  margin-top: 30px;

  padding-bottom: 5px;

  border-bottom:
    1px solid #292625;
}

.underlined-link:hover {
  color: #a57c73;

  border-color: #a57c73;
}


/* =========================
   SKILLS
========================= */

.skill-list {
  display: flex;

  flex-wrap: wrap;

  gap: 12px;

  margin-top: 65px;
}


/* =========================
   EDUCATION
========================= */

.education-section {
  padding: 140px 0;

  border-top:
    1px solid #dfd9d4;
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

  font-family:
    'Playfair Display',
    serif;

  font-size:
    clamp(42px, 6vw, 76px);

  font-weight: 400;

  line-height: 1.05;

  letter-spacing: -2px;
}

.section-heading h2 em,
.heading-row h2 em,
.languages-heading h2 em {
  color: #a57c73;
}

.section-heading p {
  max-width: 550px;

  margin-top: 25px;

  color: #77706c;

  font-size: 15px;

  line-height: 1.8;
}


/* =========================
   EDUCATION CARDS
========================= */

.education-grid {
  display: grid;

  grid-template-columns:
    1.25fr
    .75fr;

  gap: 24px;
}

.education-card {
  position: relative;

  min-height: 470px;

  padding: 35px;

  overflow: hidden;

  background: #eee8e3;

  border:
    1px solid rgba(130,105,95,.12);

  transition:
    transform .4s ease,
    box-shadow .4s ease;
}

.education-card:hover {
  transform:
    translateY(-8px);

  box-shadow:
    0 25px 60px
    rgba(70,50,45,.12);
}

.education-card.featured {
  background:
    linear-gradient(
      135deg,
      #292625,
      #3b3330 60%,
      #544541
    );

  color: white;
}

.card-top {
  display: flex;

  align-items: center;

  justify-content: space-between;
}

.card-number {
  font-family:
    'Playfair Display',
    serif;

  font-size: 20px;

  color: #a57c73;
}

.featured .card-number {
  color: #d8a99c;
}

.status {
  display: flex;

  align-items: center;

  gap: 7px;

  color: #d8a99c;

  font-size: 9px;

  letter-spacing: 1.8px;
}

.status-dot {
  width: 6px;

  height: 6px;

  border-radius: 50%;

  background: #d8a99c;
}

.mini-label {
  color: #817873;

  font-size: 9px;

  letter-spacing: 1.8px;
}

.card-icon,
.small-icon {
  display: flex;

  align-items: center;

  justify-content: center;

  margin-top: 45px;

  border-radius: 50%;
}

.card-icon {
  width: 58px;

  height: 58px;

  background: #d8a99c;

  color: #292625;

  font-size: 25px;
}

.small-icon {
  width: 48px;

  height: 48px;

  background: #292625;

  color: white;
}

.date {
  display: block;

  margin-top: 25px;

  color: #a57c73;

  font-size: 11px;

  letter-spacing: 1px;

  text-transform: uppercase;
}

.featured .date {
  color: #d8a99c;
}

.education-card h3 {
  margin:
    12px 0
    18px;

  font-family:
    'Playfair Display',
    serif;

  font-size:
    clamp(30px, 4vw, 45px);

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


/* EDUCATION STATUS */

.education-status {
  display: flex;

  flex-direction: column;

  gap: 7px;

  margin-top: 20px;

  color: #d8a99c;

  font-size: 11px;
}


/* TAGS */

.tags {
  display: flex;

  flex-wrap: wrap;

  gap: 8px;

  margin-top: 25px;
}

.tags span {
  padding:
    7px
    11px;

  border:
    1px solid #d1c4be;

  color: #756e6a;

  font-size: 10px;
}

.featured .tags span {
  border-color:
    rgba(255,255,255,.18);

  color: #d9cfcb;
}


/* COURSE */

.course-provider {
  display: flex;

  flex-direction: column;

  gap: 5px;

  margin-top: 20px;
    

  padding-top: 20px;


  border-top:
    1px solid #d6cbc5;
}

.course-provider span {
  color: #817873;

  font-size: 9px;

  text-transform: uppercase;

  letter-spacing: 1.5px;
}

.course-provider strong {
  color: #292625;

  font-size: 13px;
}

.card-decoration {
  position: absolute;

  right: -20px;

  bottom: -55px;

  font-family:
    'Playfair Display',
    serif;

  font-size: 180px;

  color:
    rgba(255,255,255,.035);
}


/* =========================
   EXPERIENCE
========================= */

.experience-section {
  padding: 140px 0;

  border-top:
    1px solid #dfd9d4;
}

.heading-row {
  display: grid;

  grid-template-columns:
    1fr
    .65fr;

  gap: 80px;

  align-items: end;

  margin-bottom: 70px;
}

.heading-row h2 {
  max-width: 700px;

  margin: 0;

  font-family:
    'Playfair Display',
    serif;

  font-size:
    clamp(45px, 6vw, 78px);

  font-weight: 400;

  line-height: 1;
}

.heading-row > p {
  margin: 0;

  color: #77706c;

  font-size: 14px;

  line-height: 1.8;
}

.experience-list {
  display: flex;

  flex-direction: column;

  gap: 18px;
}

.experience-card {
  position: relative;

  display: grid;

  grid-template-columns:
    100px
    1fr
    60px;

  gap: 30px;

  min-height: 280px;

  padding: 35px;

  transition:
    transform .4s ease,
    box-shadow .4s ease;
}

.experience-card:hover {
  transform:
    translateX(8px);

  box-shadow:
    0 25px 55px
    rgba(70,50,45,.12);
}

.experience-card.rose {
  background:
    linear-gradient(
      110deg,
      #ead9d4,
      #f2e7e2
    );
}

.experience-card.green {
  background:
    linear-gradient(
      110deg,
      #dce5dd,
      #edf1eb
    );
}

.experience-card.lavender {
  background:
    linear-gradient(
      110deg,
      #e4ddec,
      #f0edf5
    );
}

.experience-number {
  font-family:
    'Playfair Display',
    serif;

  font-size: 22px;

  color: #a57c73;
}

.experience-main {
  max-width: 720px;
}

.experience-meta {
  display: flex;

  flex-wrap: wrap;

  gap: 10px;

  color: #817873;

  font-size: 10px;

  text-transform: uppercase;

  letter-spacing: 1.4px;
}

.experience-main h3 {
  margin:
    18px 0;

  font-family:
    'Playfair Display',
    serif;

  font-size:
    clamp(32px, 4vw, 52px);

  font-weight: 400;

  line-height: 1;
}

.experience-main p {
  max-width: 600px;

  margin: 0;

  color: #716966;

  font-size: 14px;

  line-height: 1.8;
}

.experience-tags {
  display: flex;

  flex-wrap: wrap;

  gap: 8px;

  margin-top: 25px;
}

.experience-tags span {
  padding:
    7px
    12px;

  border:
    1px solid
    rgba(100,80,75,.2);

  color: #665b57;

  font-size: 10px;
}


/* EXPERIENCE ARROW */

.arrow {
  width: 48px;

  height: 48px;

  display: flex;

  align-items: center;

  justify-content: center;

  border-radius: 50%;

  background: #292625;

  color: white;

  transition:
    transform .3s ease,
    background .3s ease;
}

.arrow:hover {
  background: #a57c73;
}

.experience-card:hover .arrow {
  transform:
    rotate(45deg);
}


/* =========================
   PROJECTS
========================= */

.projects {
  display: grid;

  grid-template-columns:
    repeat(2, 1fr);

  gap: 25px;

  margin-top: 65px;
}


/* =========================
   LANGUAGES
========================= */

.languages-section {
  padding:
    140px 0;

  border-top:
    1px solid #dfd9d4;
}

.languages-heading {
  max-width: 700px;

  margin-bottom: 60px;
}

.languages-heading h2 {
  margin: 0;

  font-family:
    'Playfair Display',
    serif;

  font-size:
    clamp(42px, 6vw, 76px);

  font-weight: 400;

  line-height: 1.05;

  letter-spacing: -2px;
}

.language-grid {
  display: grid;

  grid-template-columns:
    repeat(3, 1fr);

  gap: 18px;
}

.language-card {
  position: relative;

  display: flex;

  flex-direction: column;

  min-height: 180px;

  padding: 28px;

  background: #eee8e3;

  border:
    1px solid
    rgba(130,105,95,.12);

  transition:
    transform .3s ease,
    background .3s ease;
}

.language-card:hover {
  transform:
    translateY(-6px);

  background: #e8ddd7;
}

.language-card > span {
  color: #a57c73;

  font-family:
    'Playfair Display',
    serif;

  font-size: 18px;
}

.language-card strong {
  margin-top: auto;

  font-family:
    'Playfair Display',
    serif;

  font-size: 32px;

  font-weight: 400;
}

.language-card i {
  position: absolute;

  top: 25px;

  right: 25px;

  color: #a57c73;

  font-style: normal;
}


/* =========================
   CONTACT
========================= */

.contact {
  text-align: center;
}


/* =========================
   FOOTER
========================= */

footer {
  display: flex;

  justify-content: space-between;

  align-items: center;

  padding:
    30px 0;

  border-top:
    1px solid #dfd9d4;

  color: #817a76;

  font-size: 12px;
}

.footer-links {
  display: flex;

  gap: 25px;
}

.footer-links a:hover {
  color: #a57c73;
}


/* =========================
   RESPONSIVE
========================= */

@media (max-width: 1000px) {

  .hero {
    gap: 40px;
  }

  .hero-copy {
    padding-left: 0;
  }

  .education-grid {
    grid-template-columns: 1fr;
  }

}


@media (max-width: 900px) {

  .page {
    padding:
      0 25px;
  }

  .hero {
    grid-template-columns: 1fr;

    padding:
      70px 0;
  }

  .hero-visual {
    margin-top: 40px;
  }

  .about-content {
    grid-template-columns: 1fr;

    gap: 50px;
  }

  .heading-row {
    grid-template-columns: 1fr;

    gap: 25px;
  }

  .experience-card {
    grid-template-columns:
      50px
      1fr
      45px;

    gap: 15px;

    padding: 25px;
  }

  .projects {
    grid-template-columns: 1fr;
  }

  .language-grid {
    grid-template-columns: 1fr;
  }

}


@media (max-width: 600px) {

  .hero {
    min-height: auto;
  }

  .hero h1 {
    letter-spacing: -2px;
  }

  .hero-actions {
    align-items: stretch;

    flex-direction: column;
  }

  .button.primary,
  .button.text {
    width: fit-content;
  }

  .hero-meta {
    flex-direction: column;

    gap: 20px;
  }

  .education-section,
  .experience-section,
  .languages-section {
    padding:
      90px 0;
  }

  .education-card {
    min-height: 430px;

    padding: 28px;
  }

  .experience-card {
    grid-template-columns: 1fr;

    gap: 18px;
  }

  .experience-number {
    font-size: 18px;
  }

  .arrow {
    position: absolute;

    top: 25px;

    right: 25px;
  }

  footer {
    flex-direction: column;

    align-items: flex-start;

    gap: 20px;
  }

  .footer-links {
    flex-wrap: wrap;
  }

}
</style>
