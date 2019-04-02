<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from './components/layout/Header';
export default {
  name:"app",
  components: {
    Header
  }
}
</script>


<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }
  .btn {
    display: inline-block;
    border: none;
    background: #555;
    color: #fff;
    padding: 7px 20px;
    cursor: pointer;
  }
  .btn:hover {
    background: #666;
  }

  ::-webkit-scrollbar {
  	width: 5px;
  	height: 5px;
  }
  ::-webkit-scrollbar-button {
  	width: 0;
  	height: 0;
  }
  ::-webkit-scrollbar-corner {
  	background-color: transparent;
  }
  ::-webkit-scrollbar-thumb {
  	background-color: $color_bombay_approx;
  	border: 0 none $alabaster;
  	border-radius: 50px;
  	
  }
  ::-webkit-scrollbar-track {
  	background-color: $alabaster;
  	border: 0 none $white;
  	border-radius: 50px;
  }
</style>
