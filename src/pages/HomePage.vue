<script>
import BaseButton from "@/components/BaseButton.vue";
import Colors from "@/utils/Colors";

export default {
    components: {
        BaseButton
    },
    data () {
        return {
            color: Colors
        }
    }
}
</script>

<template>
    <div>
        <BaseButton title="BaseButton custom margin" />
        <BaseButton title="BaseButton disabled" disabled/>
        <BaseButton title="BaseButton disabled" :color=color.WARN />
        <BaseButton title="BaseButton disabled" :color=color.DANGER />
    </div>
</template>