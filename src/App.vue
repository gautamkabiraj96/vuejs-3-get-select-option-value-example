<script setup>
import { ref } from 'vue'

const selectedValue = ref('')

const onSelectChange = (e) => {
  selectedValue.value = e.target.value
}
</script>

<template>
<div>
  <label for="gender-selection">Select gender</label>
<select
  name="gender-selection"
  @change="onSelectChange(e)"
  v-model="selectedValue"
>
  <option value="0">Male</option>
  <option value="1">Female</option>
  <option value="2">Other</option>
</select>
  <p>Selected value: {{selectedValue}}</p>
</div>
</template>
