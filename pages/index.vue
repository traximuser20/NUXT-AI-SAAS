<template>
  <div class="text-black">
    {{ user }}
  </div>
</template>

<script lang="ts" setup>
const user: any = useSupabaseUser();
</script>

<style scoped></style>
