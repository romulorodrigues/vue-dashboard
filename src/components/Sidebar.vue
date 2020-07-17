<template>
     <!-- Sidebar -->
        <div id="sidebar-wrapper">
            <ul class="sidebar-nav">
                <li class="sidebar-avatar">
                    <div class="avatar">
                    </div>
                    <h3 class="avatar-name">
                        Rômulo Rodrigues
                    </h3>
                </li>
                <li>
                    <router-link to='/dashboard'><i class="icofont-dashboard-web"></i> Lorem ipsum</router-link>
                </li>
                <li>
                    <a href="#" v-on:click.prevent v-b-toggle.collapse-1><i class="icofont-users-alt-2"></i> Lorem ipsum <span class="caret float-right"><i class="icofont-caret-down"></i></span></a>
                    <b-collapse id="collapse-1">
                        <ul id="collapse-1">
                            <li><router-link to=''>Lorem ipsum</router-link></li>
                            <li><router-link to=''>Lorem ipsumo</router-link></li>
                        </ul>
                    </b-collapse>
                </li>
                <li>
                    <a href="#" v-on:click.prevent v-b-toggle.collapse-2><i class="icofont-ui-file"></i> Lorem ipsums <span class="caret float-right"><i class="icofont-caret-down"></i></span></a>
                    <b-collapse id="collapse-2">
                        <ul id="collapse-2">
                            <li><router-link to=''>Lorem ipsum</router-link></li>
                            <li><router-link to=''>Lorem ipsum</router-link></li>
                        </ul>
                    </b-collapse>
                </li>            
                <li>
                    <a href="#" v-on:click.prevent v-b-toggle.collapse-3><i class="icofont-users-alt-2"></i> Lorem ipsum <span class="caret float-right"><i class="icofont-caret-down"></i></span></a>
                    <b-collapse id="collapse-3">
                        <ul id="collapse-3">
                            <li><router-link to=''>Lorem ipsum</router-link></li>
                            <li><router-link to=''>Lorem ipsum</router-link></li>
                            <li><router-link to=''>Lorem ipsum</router-link></li>
                        </ul>
                    </b-collapse>
                </li>
                <li>
                    <a href="#" v-on:click.prevent v-b-toggle.collapse-4><i class="icofont-user-suited"></i> Lorem ipsum <span class="caret float-right"><i class="icofont-caret-down"></i></span></a>
                    <b-collapse id="collapse-4">
                        <ul id="collapse-4">
                            <li><router-link to=''>Lorem ipsum</router-link></li>
                            <li><router-link to=''>Lorem ipsum</router-link></li>
                        </ul>
                    </b-collapse>
                </li>
                <li>
                    <a href="#"><i class="icofont-logout"></i> Lorem ipsum</a>
                </li>
            </ul>
        </div>
        <!-- /#sidebar-wrapper -->
</template>

<script>

export default {
    name: 'Sidebar'
}
</script>

<style>

 body {
    overflow-x: hidden;
    background-color: #ECF0FA;
 }

#wrapper {
    padding-left: 0;
    -webkit-transition: all 0.5s ease;
    -moz-transition: all 0.5s ease;
    -o-transition: all 0.5s ease;
    transition: all 0.5s ease;
}

#wrapper.toggled {
    padding-left: 250px;
}

#sidebar-wrapper {
    z-index: 1000;
    position: fixed;
    left: 250px;
    width: 0;
    height: 100%;
    margin-left: -250px;
    overflow-y: auto;
    background: #fff;
    -webkit-transition: all 0.5s ease;
    -moz-transition: all 0.5s ease;
    -o-transition: all 0.5s ease;
    transition: all 0.5s ease;
}

#wrapper.toggled #sidebar-wrapper {
    width: 250px;
}

#page-content-wrapper {
    width: 100%;
    position: absolute;
}

#wrapper.toggled #page-content-wrapper {
    position: absolute;
    margin-right: -250px;
}

.sidebar-nav {
    position: absolute;
    top: 0;
    width: 250px;
    margin: 0;
    padding: 0;
    list-style: none;
}

.sidebar-nav li {
    text-indent: 20px;
    line-height: 30px;
}

.sidebar-nav li ul li {
    text-indent: 20px;
    line-height: 15px;
}

.sidebar-avatar{
    padding-bottom: 10px;
    border-bottom: 1px solid #f9f9f9;
}

.sidebar-nav li a {
    display: block;
    text-decoration: none;
    color: #5b6e88;
    padding: 10px 0;
    font-size: 19px;
    text-align: left;
}

.sidebar-nav li ul li a {
    font-size: 15px;
}

.sidebar-nav li a:hover {
    background-color: #f5f5f5;
}

.sidebar-nav li a:hover {
    text-decoration: none;
    color: #000;
}

.sidebar-nav li a:active,
.sidebar-nav li a:focus {
    text-decoration: none;
}

.sidebar-nav > .sidebar-brand {
    height: 65px;
    font-size: 18px;
    line-height: 60px;
}

.sidebar-nav > .sidebar-brand a {
    color: #999999;
}

.sidebar-nav > .sidebar-brand a:hover {
    color: #fff;
    background: none;
}

.avatar{
    width: 120px;
    height: 120px;
    border-radius: 100%;
    margin: 15px auto;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    background-color: #f5f5f5;
    border: 1px solid #DFE4F1;
    background-image: url('../assets/eu.jpg')
}

.avatar-name{
    text-align: center;
    font-size: 18px;
    margin-left: -25px;
}

.caret{
    margin-right: 10px;
}

@media(min-width:768px) {
    #wrapper {
        padding-left: 250px;
    }

    #wrapper.toggled {
        padding-left: 0;
    }

    #sidebar-wrapper {
        width: 250px;
    }

    #wrapper.toggled #sidebar-wrapper {
        width: 0;
    }

    #page-content-wrapper {
        position: relative;
    }

    #wrapper.toggled #page-content-wrapper {
        position: relative;
        margin-right: 0;
    }
}
</style>
