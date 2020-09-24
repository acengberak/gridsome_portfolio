<template>
    <div>
        <section id="contact" class="contact-section">
            <v-container>
                <v-row>
                    <v-col>
                        <h1 class="text-center">Contact Information</h1>
                    </v-col>
                </v-row>
                <v-row>
                    <v-col sm="6" offset-sm="3" class="d-flex justify-space-around">
                        <!-- <v-icon></v-icon> -->
                        <img 
                            class="contact-icon" 
                            src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/youtube.svg" 
                        >
                        <img 
                            class="contact-icon" 
                            src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" 
                        >
                        <img 
                            class="contact-icon" 
                            src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/vimeo.svg" 
                        >
                        <img 
                            class="contact-icon" 
                            src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/github.svg" 
                        >
                    </v-col>
                </v-row>
            </v-container>
        </section>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    .contact-icon {
        height: 30px;
    }
</style>