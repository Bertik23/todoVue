<template>
  <SwitchGroup>
    <div class="flex items-center">
      <Switch
        v-model="enabled"
        :class='enabled ? "bg-lime" : "bg-gray-200"'
        class="relative inline-flex items-center h-6 transition-colors rounded-md w-6"
        @click="toggle"
      >
        <span
          :class='enabled ? "hidden" : ""'
          class="inline-block w-4 h-4 transition-transform transform bg-gray-50 rounded-full translate-x-1"
        />
        <span
          :class='enabled ? "" : "hidden"'
          class="table m-auto w-4 h-4 bi bi-check-lg"
        ><i class=""></i></span>
      </Switch>
      <SwitchLabel class="mr-4"><span class="mx-1"/>{{ text }}<slot></slot></SwitchLabel>
    </div>
  </SwitchGroup>
</template>

<script>
  import { ref } from 'vue'
  import { Switch, SwitchGroup, SwitchLabel } from '@headlessui/vue'

  export default {
    components: { Switch, SwitchGroup, SwitchLabel },
    props: ["text", "toggled"],

    setup() {
      const enabled = ref(false)

      return { enabled }
    },
    mounted() {
        this.enabled = this.toggled
    },
    methods: {
        toggle() {
            console.log(window.localStorage.getItem("todoItems"))
            console.log(this.text, this.enabled)
            // [{id: 0, "text": "Ahoj jak se máš?", toggled: true}]
        }
    }
  }
</script>