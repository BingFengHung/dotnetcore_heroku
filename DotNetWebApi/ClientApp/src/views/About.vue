<template>
  <div class="about">
    <h1>This is an about page</h1>
    <AboutComponent msg='OhYa'/>
  </div>
  
</template>


<script lang='ts'>
import { Component, Vue } from 'vue-property-decorator';
import AboutComponent from '@/components/AboutComponent.vue'; // @ is an alias to /src

@Component({
  components: {
    AboutComponent
  }
})

export default class About extends Vue {}
</script>
