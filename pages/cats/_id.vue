<template>
  <h1>Catch all numbers</h1>
</template>

<script>
export default {
  validate({params}) {
   return /^\d+$/.test(params.id)
  }
}
</script>

<style>

</style>