<template>
    <nav class="navbar pb-0 navbar-expand bg-transparent navbar-light border-bottom-1 my-2">
        <nuxt-link v-if="$store.state.editMode" :to="{name: 'admin-create'}" class="createbtn">+</nuxt-link>
        <nuxt-link class="navbar-brand ml-sm-4 ml-1" to="/admin">SimpleVids</nuxt-link>

        <div class="collapse navbar-collapse">
            <ul class="navbar-nav ml-auto mt-2 mt-lg-0">
                <li class="nav-item">
                    <nuxt-link to="/contact-us">Contact us</nuxt-link>
                </li>
                <li class="nav-item">
                    <nuxt-link to="/about-us">About us</nuxt-link>
                </li>
                <button
                    class="btn text-white ml-auto mr-2 btn-sm"
                    @click="$store.commit('logout')"
                >Logout</button>
            </ul>
        </div>
    </nav>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
.navbar-brand {
    color: #de9b37 !important;
    font-size: 40px;
    font-weight: 700;
    @media screen and (max-width: 550px) {
        font-size: 35px;
    }
    @media screen and (max-width: 420px) {
        font-size: 28px;
    }
}
.createbtn {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: #f6f6f6;
    color: #2a3744;
    position: fixed;
    right: 5%;
    bottom: 5%;
    z-index: 10000;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 30px;
    text-decoration: none;
    transition: all 0.2s;
    box-shadow: 0 2px 5px #777;
    &:hover {
        background: #47a3ef;
        color: white;
    }
}
.btn {
    background: #de9b37;
}
.btn-group {
    .btn {
        @media screen and (max-width: 550px) {
            font-size: 12px !important;
        }
        span {
            @media screen and (max-width: 520px) {
                display: none;
            }
        }
        @media screen and (max-width: 420px) {
            font-size: 10px !important;
            padding-left: 7px;
            padding-right: 7px;
        }
    }
}
</style>
