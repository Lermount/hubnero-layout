<template>
    <header id="header">
        <div class="header-left">
            <Burger />
            <h1 class="title">Team</h1>
        </div>

        <div class="header-right">
            <Search />
            <Notification />
            <User />
        </div>
    </header>
</template>
<script>
import Burger from '@/components/header/burger-menu.vue';
import Search from '@/components/header/header-search.vue';
import Notification from '@/components/header/header-notification.vue';
import User from '@/components/header/header-user.vue';

export default {
    components: {
        Burger,
        Search,
        Notification,
        User
    }
}
</script>
<style scoped>
#header {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 22px 28px;
    background: #fff;
    border-top-right-radius: 16px;
}

#header::before {
    display: block;
    position: absolute;
    content: '';
    top: 0;
    left: 0;
    width: 28px;
    height: 100%;
    background: linear-gradient(90deg, rgba(42, 53, 90, 0.04) 0%, rgba(42, 53, 90, 0) 100%);
}

.header-left,
.header-right {
    display: flex;
    align-items: center;
}

.title {
    font-family: Commissioner-Medium;
    font-size: 22px;
    font-weight: 500;
    line-height: 33px;
    letter-spacing: 0px;
    text-align: left;
    color: #2A355A;
}

@media(max-width: 600px) {
    #header {
        border-top-left-radius: 16px;
    }
}
</style>