<!-- App.vue -->
<template>
  <div class="w-full min-h-screen flex items-center">
    <div class="mx-auto w-full max-w-[800px]">
      <Card>
        <CardTitle>
          <h1 class="text-3xl font-bold text-center pt-4">Welcome</h1>
        </CardTitle>
        <CardContent>
          <Auth
            :supabaseClient="supabaseClient"
            :appearance="{
              theme: ThemeSupa,
            }"
            :providers="['google', 'github']"
            redirectTo="/"
          />
        </CardContent>
      </Card>
    </div>
  </div>
</template>

<script setup lang="ts">
// Import predefined theme
import { ThemeSupa } from "@supabase/auth-ui-shared";
import { Auth } from "@nuxtbase/auth-ui-vue";

const supabaseClient = useSupabaseClient();

definePageMeta({
  layouts: "home",
});
</script>

<style scoped></style>
