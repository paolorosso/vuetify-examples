<template>
  <v-dialog v-model="getDialog" max-width="1200px"></v-dialog>
</template>

<script>
export default {
  props: {
    dialog: { type: Boolean, required: true, default: false }
  },

  methods: {
    close() {
      this.$emit("close");
    }
  },

  computed: {
    getDialog: {
      get: function() {
        return this.dialog;
      },
      set: function(value) {
        if (!value) {
          this.close();
        }
      }
    }
  }
};
</script>


