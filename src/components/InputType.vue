<template>
  <textarea :name="data.name" v-if="data.type === 'textarea'" :id="data.name"></textarea>
  <select :name="data.name" :id="data.name" v-else-if="data.type === 'select'">
    <option :value="item.value" v-for="item in data.items" :key="item.value">{{item.label}}</option>
  </select>
  <input :type="data.type" :id="data.name" :name="data.name" v-else>
</template>

<script>
export default {
  props: ['data'],
};
</script>
