<template>
    <base-button
        title="Disabled and animated for 2 seconds if clicked"
        :disabled="isPending"
        :color="color"
        @click.stop.prevent="count++;handleClick()"
    />
</template>

<script>
    import BaseButton from './BaseButton.vue'
  
    export default {
        name: 'AsyncButton',
        components: { BaseButton },
        inheritAttrs: false,
        props: {
            color: String
        },
        data () {
            return {
                isPending: false,
                count: 0
            }
        },
        methods: {
            handleClick () {
                this.isPending = true
                new Promise(() => {
                    setTimeout(() => {
                        this.isPending = false
                    }, 2000)
                })
            }
        }
    }
</script>
