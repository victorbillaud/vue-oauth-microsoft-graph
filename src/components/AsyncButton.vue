<template>
        <base-button
            :title="isPending ? 'Button loading' : 'Button waiting'"
            :color="isPending ? color.WARN : color.PRIMARY" 
            @click.prevent.stop="count++;handleClick()"
        />
</template>

<script>
    import BaseButton from './BaseButton.vue'
    import Colors from '@/utils/Colors'
  
    export default {
        name: 'AsyncButton',
        components: { BaseButton },
        inheritAttrs: false,
        data () {
            return {
                color: Colors,
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
