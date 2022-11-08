<template>
    <div class="card">
      <div v-if="loading.state" class="container-div">
        <SpinnerComponent />
      </div>
      <div v-else class="container-div">
        <AdivceNumberComponent :title="'Advise #'+quote.id"/>
        <QuoteComponent :quote="quote.advice"/>
      </div>
      
      <DividerComponent />

      <div class="button-container">
        <button @click="getAdvice()">
          <img src="./assets/icon-dice.svg" alt="dice icon">
        </button>
      </div>
    </div>
</template>
<script setup>
  import { reactive } from 'vue';

  import AdivceNumberComponent from './components/AdivceNumberComponent.vue';
  import DividerComponent from './components/DividerComponent.vue';
  import QuoteComponent from './components/QuoteComponent.vue';
  import SpinnerComponent from './components/SpinnerComponent.vue';

  const quote = reactive({
    id : '',
    advice : ''
  })

  const loading = reactive({
    state : true
  })

  const getAdvice = async () => {
    loading.state = true

    await fetch('https://api.adviceslip.com/advice')
        .then(resp => resp.json())
        .then(resp => {
          quote.id = resp.slip.id;
          quote.advice = resp.slip.advice;

          loading.state = false
        })
  }

  getAdvice()
  
</script>