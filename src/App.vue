<script setup lang="ts">
import { computed, ref } from "vue";
import MotivationalQuote from "./components/MotivationalQuote.vue";

const quotes = [
  // Marcus Aurelius
  "You have power over your mind - not outside events. Realize this, and you will find strength.",
  "When you arise in the morning think of what a privilege it is to be alive, to think, to enjoy, to love...",
  "The happiness of your life depends upon the quality of your thoughts.",
  "If it is not right do not do it; if it is not true do not say it.",
  "Whenever you are about to find fault with someone, ask yourself the following question: What fault of mine most nearly resembles the one I am about to criticize?",
  "People are not disturbed by things, but by the views they take of them.",
  "Do not indulge in dreams of having what you have not, but reckon up the chief of the blessings you do possess, and then thankfully remember how you would crave for them if they were not yours.",
  "The soul becomes dyed with the color of its thoughts.",
  "Don't go on discussing what a good person should be. Just be one.",
  "Remember that very little is needed to make a happy life.",

  // Epictetus
  "Wealth consists not in having great possessions, but in having few wants.",
  "Man is not worried by real problems so much as by his imagined anxieties about real problems.",
  "First say to yourself what you would be; and then do what you have to do.",
  "Any person capable of angering you becomes your master; he can anger you only when you permit yourself to be disturbed by him.",
  "He who laughs at himself never runs out of things to laugh at.",
  "Caretake this moment. Immerse yourself in its particulars. Respond to this person, this challenge, this deed. Quit evasions. Stop giving yourself needless trouble. It is time to really live; to fully inhabit the situation you happen to be in now.",
  "A ship should not ride on a single anchor, nor life on a single hope.",
  "It's not what happens to you, but how you react to it that matters.",
  "You become what you give your attention to.",
  "No person is free who is not master of himself.",

  // Seneca
  "It's not because things are difficult that we dare not venture. It's because we dare not venture that they are difficult.",
  "Luck is what happens when preparation meets opportunity.",
  "We suffer more often in imagination than in reality.",
  "Associate with people who are likely to improve you.",
  "Hang on to your youthful enthusiasms - you'll be able to use them better when you're older.",
  "If a man knows not to which port he sails, no wind is favorable.",
  "He suffers more than necessary, who suffers before it is necessary.",
  "The whole future lies in uncertainty: live immediately.",
  "To wish to be well is a part of becoming well.",
  "He who is brave is free.",
];

let recomputeToggle = ref(true);

const currentQuote = computed(() => {
  recomputeToggle.value;

  return quotes[Math.floor(Math.random() * quotes.length)];
});
</script>

<template>
  <main
    class="w-full h-full bg-blue-50 grid justify-items-center place-items-center"
  >
    <MotivationalQuote
      :quote="currentQuote"
      @click="recomputeToggle = !recomputeToggle"
    />
  </main>
</template>
