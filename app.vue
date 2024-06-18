<script setup lang="ts">
  const stripe = await useClientStripe()
  const elements = ref()
  if (stripe) {
    elements.value = stripe.elements() // Stripe is of type any
  }
</script>

<template>
  <div>
    <NuxtRouteAnnouncer />
    <NuxtWelcome />
  </div>
</template>
