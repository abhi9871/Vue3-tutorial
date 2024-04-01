<template>
    <img alt="Vue logo" src="./assets/logo.png">
    <div v-show="showElement">Using v-show</div>
    <template v-if="display">
    <h2>Abhishek</h2>
    <h2>Code</h2>
    <h2>Vue</h2>
  </template>
    <h2 v-if="num===0">The number is zero.</h2>
    <h2 v-else-if="num < 0">The number is negative.</h2>
    <h2 v-else-if="num > 0">The number is positive.</h2>
    <h2 v-else>Not a number.</h2>
    <h2>{{ name }}</h2>
    <div v-html="channel"></div>
    <div v-bind:id="headingId">Heading</div>
    <button v-bind:disabled="isDisabled">Bind</button>
    <h3 class="underline">Underline Text</h3>
    <h3 class="underline" v-bind:class="status">Status</h3>
    <h3 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h3>
    <h3 v-bind:class="isSoldOut ? 'soldout' : 'new'">Sold Out</h3>
    <h3 v-bind:class="['new', 'promoted']">Array Movie</h3>
    <h3 v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'new' : 'soldout']">Array Conditional Movie</h3>
    <h3 v-bind:class="{
      promoted: isPromoted,
      new: !isSoldOut,
      soldout: isSoldOut
    }">Object Conditional Movie</h3>
    <h3 v-bind:style="{color: highLightColor,
    'font-size': headerSize + 'px'}">Inline Style</h3>
    <h3 v-bind:style="headerStyleObject">Style Object</h3>
    <div v-bind:style="[baseStyleObject, successStyleObject]">Success Style</div>
    <div v-bind:style="[baseStyleObject, dangerStyleObject]">Danger Style</div>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      name: "Abhishek",
      channel: "<b>Hello Vue World!</b>",
      headingId: "heading",
      isDisabled: true,
      status: "success",
      isPromoted: true,
      isSoldOut: false,
      highLightColor: "orange",
      headerSize: 50,
      headerStyleObject: {
        color: 'orange',
        fontSize: '50px',
        padding: '20px'
      },
      baseStyleObject: {
        fontSize: '50px',
        padding: '20px',
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'white',
        border: '1px solid green'
      },
      dangerStyleObject: {
        color: 'darkred',
        backgroundColor: 'red',
        border: '1px solid darkred'
      },
      num: 0,
      display: true,
      showElement: true
    } 
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.underline {
  text-decoration: underline;
}

.success {
  color: green;
}

.promoted {
  font-style: italic;
}

.new {
  color: green;
}

.soldout {
  color: red;
}

</style>
