<template>
        <base-button
            :title="isPending ? 'Button waiting' : 'Button loading'"
            :color="color" 
            @click.prevent.stop="count++;handleClick()"
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

                const currentCount = this.count
                const promise = delay => new Promise(resolve => setTimeout(resolve, delay))

                promise(this.count*1000).finally(() => currentCount == this.count ? (this.isPending = false, this.count = 0) : this.handleClick)
            }
        }
    }
</script>
