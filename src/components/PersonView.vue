<template>
    <div class="info-panel">
      <template v-if="dude">
        <div class="emoji">{{dude.emoji}}</div>
          <div>
            <h1>{{ dude.nimi }}</h1>
            <h2><i>"{{ dude.hüüdnimi }}"</i></h2>
            <h4>{{ dude.rühm }}</h4>
          </div>
          <div>
            <InfoBar />
          </div>
        </template>
    </div>
</template>
  
<script setup>
    import { inject } from 'vue';
    import InfoBar from "./InfoBar.vue";
    
    const dude = inject("dude");
       
</script>
  
<style scoped>
    .info-panel {
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      
      padding: 3vh 4vw 16vh 4vw;
      text-align: center;
      width: 100%;
      height: 100%;
    }
    .emoji {
      font-size: 12vh;
    }
</style>