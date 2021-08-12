<template>
  <div id="Form">
    <div class="container">
      <div class="d-flex justify-content-center mt-5 pt-5">
        <input
          class="formInput px-3 mx-3"
          placeholder="Ingrese una nueva tarea"
          v-model="newItem"
        />
        <button @click="addItem" type="button" class="formBtn">Crear</button>
      </div>
      <h2 class="listTitle mt-5">Lista</h2>
      <div class="listContainer d-flex justify-content-center flex-wrap px-5 mx-5">
        <ul class="list mx-auto" v-for="(item, $index) in items" :key="$index">
          <li class="listItem">{{ $index }} {{ item }}</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Form',
  data: () => ({
    items: []
  }),

  methods: {
    addItem() {
      this.items.push(this.newItem)
      this.newItem = ''
    }
  }
}
</script>

<style>
.formBtn {
  width: 200px;
  height: 30px;
background: rgba(235, 250, 97, 0.733);
box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
backdrop-filter: blur( 9.5px );
-webkit-backdrop-filter: blur( 9.5px );
border-radius: 10px;
}

.container {
background: rgba( 202, 240, 248, 0.20 );
box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
backdrop-filter: blur( 9.5px );
-webkit-backdrop-filter: blur( 9.5px );
border-radius: 10px;
}

.formInput {
background: rgba(255, 253, 108, 0.329);
box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
backdrop-filter: blur( 9.5px );
-webkit-backdrop-filter: blur( 9.5px );
border-radius: 10px;
}

.listTitle {
  text-align: center;
}
</style>
