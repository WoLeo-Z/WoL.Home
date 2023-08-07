<template>
    <div class="my-12 px-4 text-caption" style="opacity: 0.75">
        <b>WoL's Website</b>
        <br />Created by WoL with ♥ since 2022.
        <br />Source: <a href="https://github.com/WoLeo-Z/WoL.Home">GitHub</a>
        <br />
        <br />Special Thanks: <a href="https://github.com/FlyingSky-CN/FSky7.Home">FSky7.Home</a>
        <br />
        <br />&copy; 2022-{{ year() }} WoL.
        <v-dialog v-model="dialog" max-width="768px" :dark="dark">
            <template v-slot:activator="{ on, attrs }">
                <a v-bind="attrs" v-on="on"><strong> 隐私政策 Privacy Policy. </strong></a>
            </template>
            <v-card :dark="dark">
                <f-privacy-policy></f-privacy-policy>
                <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn color="primary" text @click="dialog = false">
                        I accept
                    </v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>
    </div>
</template>

<script>
import FPrivacyPolicy from "./PrivacyPolicy";

export default {
    components: {
        FPrivacyPolicy,
    },

    data: () => ({
        dialog: false,
    }),

    props: {
        dark: {
            type: Boolean,
            required: true,
        },
    },

    methods: {
        year() {
            return new Date().getFullYear();
        },
    },
};
</script>