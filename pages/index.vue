<template>
  <img src="/assets/img/background.jpeg" width="100%" alt="" />
  <div class="container-fluid">
    <div class="row">
      <h3 class="text-center pt-3">Berita</h3>
      <div v-for="(get, i) in berita" :key="i" class="col-lg-4 pt-5 pb-5">
        <div class="card" style="width: 18rem">
          <img :src="get.foto" class="card-img-top" alt="..." />
          <div class="card-body">
            <p class="card-text">
              {{ get.nama }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const supabase = useSupabaseClient();

const berita = ref([]);

const getData = async () => {
  const { data } = await supabase.from("berita").select(`*`);
  if (data) berita.value = data;
};

onMounted(() => {
  getData();
});
</script>
