<template>
  <div>
    <NuxtRouteAnnouncer />
    <NuxtWelcome />
  </div>
</template>
<script lang="js">

export default defineComponent({
  setup() {
    const a = new SharedArrayBuffer(1024)
    console.log(a)
    return {}
  }
})

</script>