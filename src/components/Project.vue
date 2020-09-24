<template>
  <div>
    <section>
      <v-container class="project-section">
        <v-row>
          <v-col>
            <h1>Projects</h1>
          </v-col>
        </v-row>
        <Motion />
        <WebDev />
      </v-container>
    </section>
  </div>
</template>

<script>
import Motion from '@/components/pages/Motion.vue';
import WebDev from '@/components/pages/Web.vue';
export default {
    data() {
        return {
            
        }
    },
    components: {
        Motion,
        WebDev
    }
};
</script>

<style scoped>
  .project-section {
    background-color: #FCF9EC;
  }

  .project-section h1 {
    color: #0D0221;
  }

  
</style>