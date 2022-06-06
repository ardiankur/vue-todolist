<template>
  <div id="app">
    <div class="container mt-5">
      <div class="row header mb-3 p-3">
        <div class="col-lg-12">
          <h2>What I Do Today ?</h2>
        </div>
      </div>
      <div class="row content">
        <div class="col-lg-12">
          <div class="pekerjaan-rumah">
            <div class="row">
              <div v-for="tugasSaya in tugas" v-bind:key="tugasSaya.id" class="tugas mb-3 col-lg-12 text-start">
                <ItemTugas v-bind:tugasSaya="tugasSaya" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "bootstrap/dist/css/bootstrap.css";
import ItemTugas from "./components/ItemTugas.vue";

export default {
  name: "app",
  data() {
    return {
      tugas: [
        {
          id: 1,
          namaTugas: "Membersihkan Toilet",
          isDone: false,
        },
        {
          id: 2,
          namaTugas: "Membersihkan Ruang Tamu",
          isDone: false,
        },
        {
          id: 3,
          namaTugas: "Membersihkan Kamar Tidur",
          isDone: false,
        },
        {
          id: 4,
          namaTugas: "Istirahat",
          isDone: false,
        },
      ],
    };
  },
  components: { ItemTugas },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

.header {
  background: #1abc9c;
}

.header h2 {
  margin: 0;
  text-align: center;
}

.tugas .item {
  font-size: 20px;
}

.item-completed {
  color: #1abc9c;
}
</style>
