<template>
    <div class="bar">
    <RouterLink to="/">
        <img class="stickimg" src="https://github.com/MatveyVue/icopn/blob/main/Sticker1.png?raw=true">
        <button class="stickbtn">Stickers</button>
    </RouterLink>
    <RouterLink to="market">
        <img class="mrkimg" src="https://github.com/MatveyVue/icopn/blob/main/Market2.png?raw=true">
        <button class="mrkbtn">Market</button>
    </RouterLink>
    <RouterLink to="profile">
        <img class="prfimg" src="https://github.com/MatveyVue/icopn/blob/main/Profile1.png?raw=true">
        <button class="prfbtn">Profile</button>
    </RouterLink>
    </div>
</template>

<style scoped>
.stickbtn {
    color: rgb(43, 43, 43);
}

.mrkbtn {
    color: rgb(36, 133, 218);
}
</style>