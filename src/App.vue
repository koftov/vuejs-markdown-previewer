<template>
  <div id="app">
    <i-container class="container">
      <i-row>
        <i-column sm="6" class="border-right">
          <h1>Markdown</h1>
          <i-textarea v-model="text" placeholder="Enter Markdown Here" />
        </i-column>
        <i-column sm="6">
          <h1>Formated Text</h1>
          <VueMarkdown :source="text">{{ text }}</VueMarkdown>
        </i-column>
      </i-row>
    </i-container>
  </div>
</template>

<script>
import VueMarkdown from 'vue-markdown';
export default {
  name: 'App',
  components: {
    VueMarkdown,
  },
  data() {
    return {
      text: '',
    };
  },
};
</script>

<style>
.container {
  margin-top: 40px;
}
.border-right {
  border-right: 1px dotted;
}
.form-input {
  height: 400px;
}
</style>
