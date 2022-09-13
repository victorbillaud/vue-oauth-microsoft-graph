<script>
export default {
    props: {
        title: String,
        disabled: Boolean
    }
}
</script>

<template>
    <button :disabled=disabled >{{title}}</button>
</template>

<style scoped>
    button {
        background-color: rgb(75, 180, 75);
        padding: 1em;
        margin: 0.5em;
        border: none;
        border-radius: 5px;
        font-weight: 500;
        color: white;
        cursor: pointer;
    }

    button:disabled {
        opacity: 0.5;
        cursor: cell;
    }

</style>