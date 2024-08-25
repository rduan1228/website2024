<template>
  <div class="faq">
      <h1 class="title">FREQUENTLY ASKED QUESTIONS</h1>
      <div class="faq-wrapper">
        <div v-for="(item, index) in faqItems" :key="index" class="faq-item">
          <h2 class="question">{{ item.question }}</h2>
          <p class="answer">{{ item.answer }}</p>
        </div>
      </div>
  </div>

</template>

<script>
export default {
  data() {
    return {
      faqItems: [
        {
          question: "WHAT IS A HACK-A-THON?",
          answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
        },
        {
          question: "WHO CAN ATTEND?",
          answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
        },
        {
          question: "IS HACK WASHU IN-PERSON?",
          answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
        },
        {
          question: "IS HACK WASHU FREE?",
          answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
        },
        {
          question: "I CAN'T CODE, SHOULD I STILL COME?",
          answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
        },
        {
          question: "I HAVE MORE QUESTIONS!!",
          answer: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
        }
      ]
    };
  }
};
</script>

<style scoped>
.faq {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 2rem;
  margin: 0 auto;
  font-family: 'Open Sans', sans-serif;
  border-bottom: 0.25vw solid black;
  width: 100vw;
}

.title {
  font-size: 3.175vw;
  font-weight: 400;
  font-family: 'pf-videotext';
  text-align: center;
  margin: 4rem 0;
}

.faq-wrapper {
  max-width: 600px;
  width: 100%;
  margin-bottom: 1.5rem;
}

.faq-item {
  margin-bottom: 1.5rem;
  text-align: left;
}

.question {
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
  font-family: 'pf-videotext';
  text-align: left;
  line-height: 1.5;
  font-weight: 400;

}

.answer {
  font-size: 1rem;
  text-align: left;
  line-height: 1.5;
}

@media (max-width: 600px) {
  .title {
    font-size: 1.5rem;
  }

  .question {
    font-size: 1rem;
  }

  .answer {
    font-size: 0.875rem;
  }
}
</style>

