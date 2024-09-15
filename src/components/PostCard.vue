<template>
  <div class="post-card">
    <h2>{{ title }}</h2> 
    <p>{{ body }}</p> 
  </div>
</template>

<script>
export default {
  name: "PostCard",
  props: {
    title: {
      type: String,
      required: true, 
    },
    body: {
      type: String,
      required: true, 
    },
  },
};
</script>

<style scoped>
.post-card {
  background-color: #f9f9f9;
  width: 300px;
  padding: 20px;
  margin: 10px;
  border-radius: 8px;
  border: 1px solid #ddd;
  box-shadow: 2px 2px 10px rgba(90, 14, 14, 0.1);
}

h2 {
  color:red;
  font-size: 1.2rem;
  margin-bottom: 10px;
}

p {
  color: #555;
  font-size: 1rem;
  line-height: 1.5;
}
</style>
