<template>
     <b-navbar toggleable="lg" type="dark">
        
        <b-navbar-brand href="#" v-on:click.prevent.stop="$emit('toggle')">
            <i class="icofont-navigation-menu"></i>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        
        <b-collapse id="nav-collapse" is-nav class="d-none d-lg-block">
            <b-navbar-nav>
                <b-nav-item href="#">
                    <b-nav-form>
                    <b-form-input size="sm" class="mr-sm-2" placeholder=""></b-form-input>
                    <b-button size="sm" class="my-2 my-sm-0" type="submit">Lorem ipsum</b-button>
                    </b-nav-form>
                </b-nav-item>
            </b-navbar-nav>

            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
                <b-nav-item-dropdown right>
                    <template v-slot:button-content>
                        <i class="icofont-ui-user"></i>
                    </template>
                    <b-dropdown-item href="#"><i class="icofont-tools"></i> Lorem ipsum</b-dropdown-item>
                    <b-dropdown-item href="#"><i class="icofont-logout"></i> Lorem ipsum</b-dropdown-item>
                </b-nav-item-dropdown>
            </b-navbar-nav>
        </b-collapse>

    </b-navbar>
</template>

<script>

export default {
    name: 'Topbar'
}
</script>

<style>
.navbar{
    background-color: #fff;
    border-bottom: 1px solid #dee4ec;
    box-shadow: 5px 7px 26px -5px #cdd4e7;
}
.navbar .nav-link{
    color: #5b6e88 !important;
}
.navbar a i{
    color: #5b6e88;
    font-size: 20px;
}

@media(max-width: 768px){
    .navbar-dark .navbar-toggler {
        border-color:transparent;
    }
}
</style>
