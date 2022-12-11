<template>
  <div class="mx-auto">
    <h2 class="mt-4">My Indenticon Generator</h2>
    <div class="max-w-4xl mt-5 rounded border space-y-3 bg-gray-100 mx-auto grid grid-cols-6 gap-6">
      <div class="col-span-6 sm:col-span-6">
        <label for="input" class="block text-sm font-medium text-gray-700">Input</label>
        <input type="text" name="input" id="input"
               @input="onInput"
               class="mt-1 block w-full border-gray-300 shadow-sm focus:border-indigo-500 focus:ring-indigo-500">
      </div>
      <div class="col-span-6 sm:col-span-6 mx-auto">
        <label for="output" class="block text-sm font-medium text-gray-700">Output</label>
        <div v-html="identicon"/>
      </div>
    </div>
  </div>
</template>
<script>
import jdenticon from 'jdenticon';
export default {
  components: {},
  data() {
    return {
      textInput: ''
    }
  },
  computed: {
    identicon() {
      return jdenticon.toSvg(this.textInput, 200);
    },
  },
  methods: {
    onInput(event) {
      this.textInput = event.target.value;
    }
  }
}
</script>