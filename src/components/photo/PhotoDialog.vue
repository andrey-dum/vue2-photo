<template>
    <v-dialog
        v-model="dialogVisible"
        max-width="600"
    >
       <v-card>
           <v-card-title>{{fullTitle}}</v-card-title>
           <v-card-text>
               <v-img
                    :src="photo.url"
                />
           </v-card-text>
       </v-card>
    </v-dialog>
</template>

<script>
export default {
    props: {
        photo: {
            type: Object,
            required: true
        },
        value: {
            type: Boolean,
            default: false
        }
        // dialogVisible: {
        //     type: Boolean,
        //     default: false
        // }
    },
    // props: ['photo', 'dialogVisible'],
    created() {
        this.dialogVisible = this.value
    },
    data: () => ({
        dialogVisible: false
    }),
    watch: {
        value(newValue) {
            this.dialogVisible = newValue
        },
        dialogVisible(newValue) {
            this.$emit('input', newValue) 
        }
    },
    computed: {
        fullTitle() {
            return `Название - ${this.photo.title}`
        }
    }
  
  
}
</script>

<style>

</style>