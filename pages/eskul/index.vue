<template>
  <div class="container">
    <h3 class="text-center pt-3">Ekstrakurikuler</h3>
    <div class="row">
      <div v-for="(get, i) in eskul" :key="i" class="col-lg-4 pt-3 pb-3">
        <div class="card" style="width: 18rem">
          <img :src="get.poto" class="card-img-top" alt="..." />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const supabase = useSupabaseClient();

const eskul = ref([]);

const getData = async () => {
  const { data } = await supabase.from("eskul").select(`*`);
  if (data) eskul.value = data;
};
onMounted(() => {
  getData();
});
</script>
