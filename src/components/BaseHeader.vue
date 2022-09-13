<template>
    <div class="container-header">
        <h1>
            人類社会
        </h1>
        <div class="container-account">
            <img src="../assets/user.svg" alt="" width="30"/>
            <h2>
                Account
            </h2>
        </div>
    </div>
</template>

<style>
    .container-header {
        width: 100vw;
        background-color: rgb(40, 40, 40);
        font-family: 'Noto Sans JP', sans-serif;
        color: white;
        height: auto;
        margin: 0;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    .container-account {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    h1 , h2 {
        margin: 0;
        padding: 1em;
    }
    
</style>