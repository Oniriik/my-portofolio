<template>
  <div class="project" @click.prevent="projectHref">
    <img :src="img" :alt="title" />
    <div class="project-infos">
      <div class="project-title">
        <p class="project-name" :style="{ color: this.accentColor }">
          {{ title }}
        </p>
        <p class="project-stack" :style="{ backgroundColor: this.secondColor }">
          {{ stack }}
        </p>
      </div>
      <p class="project-desc">{{ desc }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    img: {
      type: String,
      required: true,
    },
    stack: {
      type: String,
      required: true,
    },
    desc: {
      type: String,
      required: true,
    },
    accentColor: {
      type: String,
      required: true,
    },
    secondColor: {
      type: String,
      required: true,
    },
    href: {
      type: String,
      required: true,
    },
  },
  methods: {
    projectHref() {
      window.open(this.href, '_blank').focus();
    },
  },
};
</script>

<style scoped>
.project {
  width: 400px;
  border-radius: 1rem;
  overflow: hidden;
  box-shadow: 3px 3px 7px rgba(0, 0, 0, 0.249);
  filter: grayscale();
  transition-duration: 0.5s;
  justify-self: center;
}
.project-infos {
  padding: 0 10px;
  padding-bottom: 10px;
}
.project > img {
  aspect-ratio: 2/1;
  width: 100%;
  filter: blur(3px);
  transition-duration: 0.5s;
}
.project:hover {
  transform: scale(1.03);
  filter: none;
  cursor: pointer;
  transition-duration: 0.5s;
}
.project:hover img {
  filter: none;
  transition: 0.5s;
}

.project-title {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 0.5rem;
}
.project-name {
  font-weight: 800;
}
.project-stack {
  font-size: 0.6rem;
  border-radius: 1rem;
  padding: 2px 6px;
  color: white;
}
.project-desc {
  margin-top: 5px;
  height: 30px;
  font-size: 0.7rem;
  font-style: italic;
  color: #858585;
}

@media (max-width: 1000px) {

    .project {
    width: 350px;
    }
    .project-name {
    font-size: 0.9rem;
    }
    .project-desc {
     font-size: 0.60rem;
    }

}
</style>