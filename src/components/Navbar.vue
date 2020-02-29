<template>
    <nav>
        <v-toolbar flat app>
            <v-toolbar-side-icon class="grey--text" @click="drawer = !drawer">
                <v-icon>
                    menu
                </v-icon>
            </v-toolbar-side-icon>
            <v-toolbar-title class="text-uppercase grey--text">
                <span class="font-weight-light ml-1">Tobias </span>
                <span>Furtlehner</span>
            </v-toolbar-title>
        </v-toolbar>

        <v-navigation-drawer temporary app v-model="drawer" class="primary">
            <v-content align-center>
                <v-avatar size="175px" class="ma-4">
                    <img src="/profile-picture.png">
                </v-avatar>
                <v-list dense>
                    <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
                        <v-list-item-action>
                            <v-icon color="white">{{ link.icon }}</v-icon>
                        </v-list-item-action>
                        <v-list-item-content>
                            <v-list-item-title class="white--text">{{ link.text }}</v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>
            </v-content>
        </v-navigation-drawer>
    </nav>
</template>

<script>
    export default {
        data() {
            return {
                drawer: false,
                links: [{
                        icon: "dashboard",
                        text: "Homepage",
                        route: "/"
                    },
                    {
                        icon: "folder",
                        text: "My Projects",
                        route: "/projects"
                    },
                    {
                        icon: "school",
                        text: "Resume",
                        route: "/resume"
                    },
                    {
                        icon: "person",
                        text: "About",
                        route: "/about"
                    }
                ]
            }
        }
    }
</script>

<style>
    .align-center {
        margin: auto;
        width: 10%;
    }
</style>