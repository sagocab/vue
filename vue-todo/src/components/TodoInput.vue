<template>
  <div class="inputBox shadow">
    <input type="text" v-model="newToItem" v-on:keyup.enter="addTodo">
    <!--button v-on:click="addTodo">add</button-->
    <span class="addContainer" v-on:click="addTodo">
      <i class="fas fa-plus addBtn"></i>
    </span>
  </div>
</template>

<script>
export default {
  data : function(){
    return {
      newToItem : ""
    }
  },
  methods : {
    addTodo : function(){
      if(this.newToItem !== ''){
        var obj = {completed: false, item:this.newToItem};
        //저장하는 로직
        localStorage.setItem(this.newToItem, JSON.stringify(obj));
        this.clearInput();
      }
    },
    clearInput : function(){
      this.newToItem = '';
    }
  }
}
</script>

<style scoped>
input:focus {
  outline: none;
}
.inputBox {
  background: white;
  height: 50px;
  line-height: 50px;
  border-radius: 5px;
}
.inputBox input {
  border-style: none;
  font-size: 0.9rem;
}
.addContainer {
  float: right;
  background: linear-gradient(to right, #6478FB, #8763FB);
  display: block;
  width: 3rem;
  border-radius: 0 5px 5px 0;
}
.addBtn {
  color: white;
  vertical-align: middle;
}
</style>