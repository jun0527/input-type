<template>
  <div class="formGroup">
    <label :for="data.name.name">{{data.name.name}}：</label>
    <input-type :data="data.name"></input-type>
  </div>
  <div class="formGroup">
    <label :for="data.description.name">{{data.description.name}}：</label>
    <input-type :data="data.description"></input-type>
  </div>
  <div class="formGroup">
    <label :for="data.select.name">{{data.select.name}}：</label>
    <input-type :data="data.select"></input-type>
  </div>
</template>

<style scoped>
  .formGroup {
    display: flex;
    margin-bottom: 16px;
  }
</style>

<script>
import inputType from '@/components/InputType.vue';

export default {
  data() {
    return {
      data: {
        name: {
          type: 'text',
          name: '名稱',
        },
        description: {
          type: 'textarea',
          name: '說明',
        },
        select: {
          type: 'select',
          name: '選擇',
          items: [
            {
              value: 1,
              label: '選項A',
            },
            {
              value: 2,
              label: '選項B',
            },
          ],
        },
      },
    };
  },
  components: {
    inputType,
  },
};
</script>
