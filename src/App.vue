<template>
  <div>
    <nav class="navbar">
      <ul>
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/about">About</router-link></li>
        <li><router-link to="/blog">Blog</router-link></li>
        <li><router-link to="/contactus">Contact Us</router-link></li>
      </ul>
    </nav>
    
    <BlogComponent/>
    <ContactComponent/>
  </div>
</template>

<script>
import BlogComponent from './components/BlogComponent.vue';
import ContactComponent from './components/ContactComponent.vue';
export default {
  name: 'App',
  components: {
    BlogComponent,
    ContactComponent
  }
}
</script>

<style>
.navbar {
  background-color:red;
  color: #fff;
  padding: 20px;
  text-align: center;
  width:100%;
margin-top:0;
}

.navbar ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: space-between;
}

.navbar li {
  margin-right: 20px;
}

.navbar a {
  color: #fff;
  text-decoration: none;
}

.navbar a:hover {
  color: #cccccc;
}


</style>