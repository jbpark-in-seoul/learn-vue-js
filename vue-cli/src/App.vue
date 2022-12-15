<template>
  <!-- 템플릿 루트(<div>태그)는 한 개만 정의되어야 함. -->
  <div>
    <!-- <app-header v-bind:프롭스 속성 이름="상위 컴포넌트의 데이터 이름"></app-header> -->
    <app-header 
    v-bind:propsdata="str"
    v-on:renew="renewStr"></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

// var AppHeader = {
//   template: '<div><h1>Header</h1></div>'
// }
export default {
  // 컴포넌트 재사용성을 위해 기존의 문법대로 `data` 속성을 정의하지 않는다.
  // new Vue({
  //   data: {
  //     str: 'hi'
  //   }
  // })
  data: function() {
    return {
      str: 'Header'
    }
  },
  components: {
    'app-header': AppHeader
  },
  methods: {
    renewStr: function() {
      this.str = 'hi';
    }
  }
}
</script>

<style>

</style>