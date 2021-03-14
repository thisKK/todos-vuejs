<template>
  <div>
    <button :class="{ active: filter == 'all' }" @click="changeFilter('all')">
      All
    </button>
    <button :class="{ active: filter == 'active' }" @click="changeFilter('active')"
    >
      Active
    </button>
    <button :class="{ active: filter == 'completed' }" @click="changeFilter('completed')"
    >
      Completed
    </button>
  </div>
</template>
<script>
export default {
  name: "todo-filtered",
  props: {},
  data() {
    return {
      filter: "all",
    };
  },
  methods: {
    changeFilter(filter) {
      this.filter = filter;
      this.$emit('filterChanged',filter)
    },
  },
};
</script>
