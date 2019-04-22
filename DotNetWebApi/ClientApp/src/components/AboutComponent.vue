<template>
  <div>
      <h2>Hello</h2>
      <h3>{{ msg }}</h3>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class AboutComponent extends Vue {
  @Prop() private msg!: string;
  mounted() {
      alert('in');
      Vue.axios.get("/api/values").then((response) => {
          alert(JSON.stringify(response));
      });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
