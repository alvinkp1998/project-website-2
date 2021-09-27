<template>
  <div>
    <div class="card shadow" style="width: 21rem;">
      <img
        height="200px"
        class="card-img-top"
        :src="img"
        alt="Card image cap"
      />
      <div class="card-body">
        <h5 class="card-title text-center">{{ name }}</h5>
      </div>
      <button
        type="button"
        class="btn btn-primary pill"
        data-toggle="modal"
        data-target=".bd-example-modal-lg"
      >
        Lihat Kelas
      </button>
      <class-modal :img="img" :name="name" :desc="desc" />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    id: { type: Number },
    name: { type: String, default: "" },
    desc: { type: String, default: "" },
    img: { type: String, default: "" }
  }
};
</script>

<style scoped>
.card {
  padding: 1.2em;
  background-color: white;
}
.pill {
  border-radius: 30px;
}
</style>
