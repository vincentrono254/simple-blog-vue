<template>
  <div class="contact-us">
    <h1>Contact us</h1>
    <form v-on:submit.prevent="greetUser" class="form">
      
      <div class="form-group">
        <label for="username">Email:</label>
        <input type="text" v-model="email" class="form-control" />
      </div>

      <div class="form-group">
        <label for="Message">Message:</label>
        <textarea v-model="message" class="form-control" rows="5"></textarea>
      </div>

      <button type="submit" class="btn-submit">Send Message</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "ContactUs",
  data() {
    return {
      email: "",
      message: "",
      submitted: false,
    };
  },
  methods: {
    greetUser() {
      this.submitted = true;
    },
  },
};
</script>

<style scoped>
.contact-us {
  max-width: 600px;
  margin: 40px auto;
  padding: 20px;
  background-color: #f9f9f9;
  border: 1px solid #ccc;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

h1 {
  text-align: center;
  color: blue;
  margin-bottom: 20px;
}

.form {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.form-group {
  margin-bottom: 20px;
}

label {
  display: block;
  margin-bottom: 10px;
}

.form-control {
  width: 100%;
  padding: 10px;
  font-size: 16px;
  border: 1px solid #ccc;
}

.btn-submit {
  background-color: #4CAF50;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.btn-submit:hover {
  background-color: #3e8e41;
}

.results {
  margin-top: 20px;
  padding: 20px;
  background-color: #f0f0f0;
  border: 1px solid #ccc;
}
</style>