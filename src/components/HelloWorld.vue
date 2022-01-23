<template>
  <div class="hello">
    <h1>{{ count }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-typescript" target="_blank" rel="noopener">typescript</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>

    <button @click="increaseCount()">Increase Count</button>
    <button @click="printMsg()">Call printMsg()</button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import HelloWorld from '@/components/common/HelloWorld.service'


type TInstance = InstanceType<typeof instance>;

const instance = Vue.extend({
  name: 'HelloWorld',
  created () {
    alert("horse")
  },
  props: {
    msg: String,
  },
  data() {
    return {
      count: 1,
    }
  },
  model: {
    prop: 'val',
  },
  methods: {
    increaseCount,
    printMsg,
  }
});

export default instance;


interface IUser {

}


/**
 * Increase count alt.
 */
function increaseCount(this: TInstance): void {
  this.count++
}


/**
 * Alert a message.
 */
function printMsg(this: TInstance) {
  HelloWorld.alertMsg(this.msg)
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped src="./HelloWorld.css"></style>
