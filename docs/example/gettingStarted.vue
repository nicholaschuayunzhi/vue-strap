<template>
  <div class="bs-docs-section" id="getting-started">
    <h1 class="page-header"><a href="#getting-started" class="anchor">Getting started</a></h1>
    <div class="bs-callout bs-callout-success">
      <h4>About this project</h4>
      <p>
        This repository contains a set of native Vue.js components based on Bootstrap's markup and CSS.
        As a result no dependency on jQuery or Bootstrap's JavaScript is required.
        The only required dependencies are:
      </p>
      <ul>
        <li><a href="http://vuejs.org/">Vue.js</a>
          (required ^1.0.8, test with 1.0.8).</li>
        <li><a href="http://getbootstrap.com/">Bootstrap CSS</a>
          (required 3.x.x, test with 3.3.5).
          VueStrap doesn't depend on a very precise version of Bootstrap. Just pull the latest.
        </li>
      </ul>
    </div>
    <h2>CommonJS</h2>
    <doc-code language="javascript">
      $ npm install vue-strap

      var VueStrap = require('vue-strap')
      Vue.use(VueStrap)
      var vm = new Vue({
        el: 'body'
      })

      VueStrap.installEvents(vm)
    </doc-code>
    <h2>ES6</h2>
    <doc-code language="javascript">
      $ npm install vue-strap

      import VueStrap from 'vue-strap'
      Vue.use(VueStrap)
      var vm = new Vue({
        el: 'body'
      })
      VueStrap.installEvents(vm)
    </doc-code>

    <h2>AMD</h2>
    <doc-code language="javascript">
      $ bower install vue-strap

      define(['vue-strap'], function(VueStrap) { Vue.use(VueStrap); ... });
    </doc-code>
    <h2>Browser globals</h2>
    <p>
      The <code>dist</code> folder contains <code>vue-strap.js</code> and <code>vue-strap.min.js</code> with
      all components exported in the <code>window.VueStrap</code> object. These bundles are also available on both the
      Bower and NPM packages.
    </p>
    <doc-code language="markup">
      <v-select :options="options"></v-select>

      <script src="path/to/vue.js"></script>
      <script src="path/to/vue-strap.js"></script>
      <script>
        Vue.use(VueStrap)
        var vm = new Vue({
          el: 'body'
        })
        VueStrap.installEvents(vm)
      </script>
    </doc-code>
  </div>
</template>
<script>
import docCode from './docCode.vue'
export default {
  components: {
    docCode
  }
}
</script>
