<template>
  <Sidebar />
</template>

<script>
import { defineComponent } from 'vue';

// Components
import Sidebar from '../components/Sidebar.vue';

export default defineComponent({
  name: 'HomeView',

  components: {
    Sidebar,
  },

});
</script>
