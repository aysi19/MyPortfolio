<script setup>
import pic2 from '@/assets/longpic.jpg'
import { ref, onMounted } from 'vue'

const hiText = ref('')
const iAmText = ref('')
const nameText = ref('')

const fullHiText = 'Hi there,'
const fullIAmText = 'I am '
const fullNameText = 'Josh Lendl Cagara'

const typeText = async (fullText, refVar, delay = 100) => {
  for (let i = 0; i < fullText.length; i++) {
    await new Promise(resolve => setTimeout(resolve, delay))
    refVar.value += fullText[i]
  }
}

onMounted(async () => {
  await typeText(fullHiText, hiText, 100)
  await typeText(fullIAmText, iAmText, 100)
  await typeText(fullNameText, nameText, 100)
})
</script>

<template>
  <div class="content-container">
    <div class="txt-container">
      <div class="text-inner">
        <p class="txt-hi">{{ hiText }}</p>
        <p class="txt-josh">{{ iAmText }}<span class="josh">{{ nameText }}</span></p>
      </div>

      <div class="logo-container">
        <font-awesome-icon :icon="['fab', 'facebook']" size="2x"/>
        <font-awesome-icon :icon="['fab', 'instagram']" size="2x"/>
        <font-awesome-icon :icon="['fab', 'github']" size="2x"/>
        <font-awesome-icon :icon="['fab', 'linkedin']" size="2x"/>
        <font-awesome-icon :icon="['far', 'envelope']" size="2x"/>
        </div>

      <a href="Resume2.pdf" download class="download-btn">
        Download CV
      </a>
    </div>

    <div class="pic-container">
      <img :src="pic2" alt="My Picture" class="profile-pic">
    </div>

  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&family=Sofia+Sans:ital,wght@0,1..1000;1,1..1000&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Alfa+Slab+One&family=Carter+One&family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&family=Sofia+Sans:ital,wght@0,1..1000;1,1..1000&display=swap');

.content-container{
    flex-direction: row;
    position: fixed;
    top: 0;
    left: 285px;
    right: 0;
    bottom: 0;
    background-color: white;
    display: flex;
    width: calc(100% - 285px);
}
.txt-container{
    margin-top: auto;
    margin-bottom: auto;
    left: 285px;
    width: calc(75% - 285px);
    background-color: white;
    display: flex;
    color: black;
    flex-direction: column;
    align-items: center;
}
.txt-hi,.txt-josh{
    display: block;
    font-size: 50px;
    font-family: 'SofiaSans', sans-serif;
}
.josh{
    font-size: 50px;
    font-weight: 400;
    font-family: 'Carter One', cursive;
}
.download-btn {
    width: 20%;
    display: block; 
    color: black;
    padding: 10px;
    text-align: center;
    font-size: 18px;
    font-weight: bold;
    border: 4px solid black;
    background-color: white;
    cursor: pointer;
    border-radius: 20px;
    transition: ease, 0.7s;
}

.download-btn:hover {
    background-color: black;
    color:white;
    width: 20%;
    border-radius: 20px;
}

input[type="radio"]:checked + .download-btn {
    background-color: black;
    color: white;
    width: 20%;
    border-radius: 20px;
}
.logo-container{
    margin-top: 10px;
    margin-bottom: 30px;
    display: flex;
    gap: 50px;
    
}
.pic-container{
    margin-top: auto;
    margin-bottom: auto;
    width: 25%;
    flex: 1;
    display: flex;
    align-items: center;
    background-color: white;
}
.profile-pic{
    border-radius: 300px;
    border: solid black 2px;
    box-shadow: 0 4px 50px rgba(0, 0, 0, 0.5);
}
.typing-text::after {
  content: '|';
  animation: blink 1s steps(1) infinite;
  margin-left: 4px;
}

@keyframes blink {
  50%{
    opacity: 0;
  }
}

</style>