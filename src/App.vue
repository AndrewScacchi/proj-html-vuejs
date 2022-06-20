<template>
  <div id="app">
    <MyHeader/>
    <MyMain/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain

}
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  // border: 1px solid red;
}
.flex-row{
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
.flex-col{
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
}
.btn {
  border:none;
  padding:15px;
  font-size: 0.75rem;
}
.btn-orange {
  background-color: #fe6601;
  color: #fefffe;
  border: 1px solid #fe6601;
  &:hover {
          color:#fe6601;
          background-color: #fefffe;
          border: 1px solid #fe6601 ;
          cursor: pointer;
        }
}
.btn-blue {
  background-color: #56509f;
  color: #fefffe;
  border: 1px solid #fefffe;
  &:hover {
          color:#56509f;
          background-color: #fefffe;
          cursor: pointer;
          border: 1px solid #56509f;
        }
}


//classes

// $sugarCane: #fefffe;
// $blazeOrange: #fe6601;




</style>
