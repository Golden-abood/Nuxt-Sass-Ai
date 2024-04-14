<template>
  <div class="flex items-center min-h-screen w-ful">
    <div class="max-w-[800px] w-full mx-auto">
      <Card>
        <CardTitle>
          <div class="py-4 font-bold text-center">Welcom</div></CardTitle
        >
        <CardContent>
          <Auth
            :supabaseClient="supabaseClient"
            :appearance="{
              theme: ThemeSupa,
            }"
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
import Card from "../components/ui/card/Card.vue";
import CardContent from "../components/ui/card/CardContent.vue";

const supabaseClient = useSupabaseClient();
</script>
