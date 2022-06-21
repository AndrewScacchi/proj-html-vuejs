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
  font-family: Arial, Helvetica, sans-serif;
}
.flex-row{
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
}
.flex-col{
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
}
.btn {
  border:none;
  padding: 10px 15px;
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
.round{
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;

        &-orange{
            background-color: #fe6601;
        }
        &-blue{
            background-color: #56509f;
        }
        &-white{
          background-color: white;
        }
        
    }
h1, h2, h3, h4, h5 {
  color: #56509f;
}  


//classes

// $sugarCane: #fefffe;
// $blazeOrange: #fe6601;




</style>
