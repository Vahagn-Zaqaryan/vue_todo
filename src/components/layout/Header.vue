<template>
  <header class="header">
      <nav class="nav-wrapper white z-depth-1">
       <div class="container">
         <a href="#" class="brand-logo black-text">TodoList</a>
         <ul id="nav-mobile" class="right hide-on-med-and-down">
           <li><router-link to="/" class="black-text">Home</router-link></li>
           <li><router-link to="/about" class="black-text">About</router-link></li>
         </ul>
       </div>
     </nav>
  </header>
</template>

<script>
export default {
  name: "Header"
}
</script>
