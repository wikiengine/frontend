<template>
    <div>
        <h1>{{ data.title }}</h1>
    </div>
  </template>
  
  <script>
  export default {
    async asyncData({ $axios, params }) {
      try {
        const response = await $axios.$get('http://localhost:4000/w/'+params.id);
        return { data: response };
      } catch (error) {
        console.error(error);
        return { data: null };
      }
    }
  }
  </script>