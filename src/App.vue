<template>
  <div id="app-container">
    <h1>Vue 3 컴포넌트 리팩터링 과제</h1>
    <hr>

    <h2>Example 1 (E01, E02, E03)</h2>
    <div class="example-box">
      <E01Instance />
      <E02Reactive />
      <E03Binding />
    </div>

    <h2>Example 2 (E04) - Directives</h2>
    <div class="example-box">
      <E04Directives />
    </div>

    <h2>Example 3 (E05) - Props / Emit</h2>
    <div class="example-box">
      <E05ParentComponent />
    </div>

    <h2>Example 4 (E06) - Provide / Inject</h2>
    <div class="example-box">
      <E06ParentComponent />
    </div>

    <h2>Example 5 (E07-E09) - API 가이드</h2>
    <div class="example-box">
      <p><b>(E09 정답 가이드)</b></p>
      <E09CompositionAPI2 title="E09 Composition API2" />
    </div>

    <h2>Example 6 (E10, E11, E12) - Ref / Reactive</h2>
    <div class="example-box">
      <E10Ref />
      <E11Reactive />
      <E12RefComponent />
    </div>

  </div>
</template>

<script setup>
import E01Instance from "@/components/example1/E-01-instance.vue";
import E02Reactive from "@/components/example1/E-02-reactive.vue";
import E03Binding from "@/components/example1/E-03-binding.vue";
import E04Directives from "@/components/example2/E-04-directives.vue";
import E05ParentComponent from "@/components/example3/ParentComponent.vue";
import E06ParentComponent from "@/components/example4/ParentComponent.vue";
import E09CompositionAPI2 from "@/components/example5/E-09-composition-API2.vue";
import E10Ref from "@/components/example6/E-10-ref.vue";
import E11Reactive from "@/components/example6/E-11-reactive.vue";
import E12RefComponent from '@/components/example6/E-12-ref-component.vue';
</script>

<style>
body {
  background-color: #f9f9f9;
}
#app-container {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  color: #2c3e50;
  max-width: 900px;
  margin: 20px auto;
  padding: 20px;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.05);
}
h1 {
  text-align: center;
  color: #42b983;
}
h2 {
  font-size: 1.3rem;
  padding-bottom: 5px;
  border-bottom: 2px solid #42b983;
  margin-top: 30px;
}
.example-box {
  padding: 15px;
  border: 1px solid #eee;
  border-radius: 5px;
  margin-top: 15px;
}
hr {
  border: 0;
  border-top: 1px solid #eee;
  margin: 25px 0;
}
</style>