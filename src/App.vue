<script setup>
import {ref} from 'vue'

let num = ref(0)

</script>

<template>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark border-bottom border-body">
        <div class="container-fluid">
            <router-link class="navbar-brand" to="/">RickApi</router-link>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <router-link class="nav-link" aria-current="page" to="/">Cards</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link class="nav-link" to="/about">Créditos</router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="main">
        <router-view></router-view>
    </div>

    <footer class="bg-dark text-light d-flex align-items-center justify-content-center w-100">
        <div>Gustavo Diniz | Unimar | ADS | {{ new Date().getFullYear() }}</div>
    </footer>
</template>

<style>

footer{
    bottom: 0;
    height: 50px;
}
</style>