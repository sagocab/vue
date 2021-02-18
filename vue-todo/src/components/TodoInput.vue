<template>
  <div class="inputBox shadow">
    <input type="text" v-model="newToItem" v-on:keyup.enter="addTodo">
    <!--button v-on:click="addTodo">add</button-->
    <span class="addContainer" v-on:click="addTodo">
      <i class="fas fa-plus addBtn"></i>
    </span>
    <!-- use the modal component, pass in the prop -->
    <Modal v-if="showModal" @close="showModal = false">
      <h3 slot="header">경고 !
          <i class="closeModalBtn fas fa-times" @click="closeModal"></i>
      </h3>
      <div slot="body">아무것도 입력하지 않았습니다.</div>
      <div slot="footer">copy right</div>
    </Modal>
  </div>

</template>

<script>
import Modal from './common/Modal.vue'

export default {
  data(){
    return {
      newToItem : "",
      showModal : false
    }
  },
  methods : {
    addTodo(){
      if(this.newToItem !== ''){
        //this.$emit('addTodoItem', this.newToItem);
        const text = this.newToItem.trim();
        this.$store.commit('addOneItem', text);
        this.clearInput();
      }else{
        this.showModal = !this.showModal
      }
    },
    clearInput(){
      this.newToItem = '';
    },
    closeModal(){
      this.showModal = false;
    }
  },
  components : {
    Modal
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
.closeModalBtn {
  color : #42b9b3
}
</style>