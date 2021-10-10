<template>
  <div>
    <div class="card rounded">
      <img
        :src="img"
        class="card-img-top"
        width="100%"
        height="200px"
        :alt="role"
      />
      <div class="row px-2">
        <div class="col">
          <h5 class="p-0 pt-2 m-0">{{ nama }}</h5>
          <p class="">{{ role }}</p>
        </div>
        <div class="col-2 d-flex align-items-center">
          <i
            class="fas fa-ellipsis-v pointer"
            data-toggle="dropdown"
            :style="`font-size:1em`"
          ></i>
          <div class="dropdown-menu">
            <a class="dropdown-item">Sunting</a>
            <a class="dropdown-item">Hapus</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    nama: String,
    role: String,
    img: String
  }
};
</script>
