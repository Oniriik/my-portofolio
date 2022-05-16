<template>
  <div class="container">
    <div class="profile-infos">
      <img
        src="https://i.ibb.co/zRFPzCj/profile-min.png"
        alt="myPhoto"
        class="myPhoto"
      />
      <div class="type">
        <p class="intro">
          {{ typeValue1 }} <span class="name">{{ typeValue2 }}</span
          >{{ typeValue3 }}
        </p>
        <span v-if="typeStatus" class="cursor" :class="{ typing: !typeStatus }"
          >&nbsp;</span
        >
      </div>
      <p class="bio">
        Curious and passionate about technology, I like to create and discover
        new things.<br />The taste of challenge and adaptability are my strong
        points.
      </p>
    </div>

    <mouseScrollAnim />
  </div>
</template>

<script>
import mouseScrollAnim from "@/components/mouseScrollAnim.vue";
export default {
  components: {
    mouseScrollAnim,
  },
  data: () => {
    return {
      typeValue1: "",
      typeValue2: "",
      typeValue3: "",
      typeStatus: true,
      typeArray: ["I'm ", "Timothé Lim", ", and I am a Junior developper !"],
      typingSpeed: 70,
      typeArrayIndex: 0,
      charIndex: 0,
    };
  },
  methods: {
    async typeText1() {
      this.typeStatus = true;
      if (this.charIndex <= this.typeArray[0].length) {
        this.typeValue1 += this.typeArray[0].charAt(this.charIndex);
        this.charIndex += 1;
        setTimeout(this.typeText1, this.typingSpeed);
      } else {
        this.charIndex = 0;
        setTimeout(this.typeText2, 200);
      }
    },
    typeText2() {
      if (this.charIndex <= this.typeArray[1].length) {
        this.typeValue2 += this.typeArray[1].charAt(this.charIndex);
        this.charIndex += 1;
        setTimeout(this.typeText2, this.typingSpeed);
      } else {
        this.charIndex = 0;
        setTimeout(this.typeText3, 150);
      }
    },
    typeText3() {
      if (this.charIndex <= this.typeArray[2].length) {
        this.typeValue3 += this.typeArray[2].charAt(this.charIndex);
        this.charIndex += 1;
        setTimeout(this.typeText3, this.typingSpeed);
      } else {
        setTimeout(() => {
          document.getElementsByClassName("bio")[0].classList.add("show");
          this.typeStatus = false;
          setTimeout(() => {
            document
              .getElementsByClassName("mouseScrollAnim")[0]
              .classList.add("show");
          }, 500);
        }, 1000);
      }
    },
  },
  created() {
    setTimeout(this.typeText1, 3000);
  },
};
</script>

<style scoped>
.cursor {
  display: inline-block;
  margin-left: 3px;
  width: 1px;
  height: 1.5rem;
  background-color: #000000;
  animation: blinkingText 1.2s infinite;
}
@keyframes blinkingText {
  0% {
    background-color: #000000;
  }
  49% {
    background-color: transparent;
  }
}
.typing {
  animation: none;
}
.type {
  display: flex;
  flex-direction: row;
  align-items: inherit;
}

.container {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  height: 100vh;
}
.profile-infos{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}
.myPhoto {
  border-radius: 50%;
  width: 20vw;
  transition-duration: 0.5s;
}
.intro {
  font-size: 2rem;
  font-family: "Mulish", sans-serif;
  text-align: center;
  font-weight: 300;
  transition-duration: 0.5s;
}
.name {
  font-weight: 700;
}
.bio {
  opacity: 0;
  text-align: center;
  color: #686868;
  font-weight: 300;
  font-size: 1rem;
}

.show {
  opacity: 1;
  transition-duration: 1s;
}

@media (max-width: 1000px) {
  .myPhoto {
    width: 30vw;
  }
}

@media (max-width: 800px) {
  .cursor {
    height: 1rem;
  }
  p {
    display: inline;
    text-align: center;
    font-size: 2rem;
  }
  .container {
    gap: 1em;
  }
  .myPhoto {
    width: 45vw;
  }
  .intro {
    font-size: 1rem;
    line-height: 0.8;
  }
  .bio {
    font-size: 0.7rem;
  }
}
</style>