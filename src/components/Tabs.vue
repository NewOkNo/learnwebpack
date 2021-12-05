<template>
  <div class="tabs">
    <ul>
      <li v-for="tab in tabArray" :key="tab.id" :class="{'is-active':tab.active}" @click="$emit('tabclick', tab.id)"><a>{{ tab.name }}</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['tabArray']
}
</script>

<style>

</style>