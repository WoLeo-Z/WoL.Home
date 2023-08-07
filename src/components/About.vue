<template>
    <v-card class="pt-4" :dark="dark" elevation="0" style="background: none;">
        <v-list-item>
            <v-list-item-content>
                <v-list-item-title class="headline">关于我</v-list-item-title>
                <v-list-item-subtitle>About Me</v-list-item-subtitle>
            </v-list-item-content>
        </v-list-item>
        <v-card-text class="f-text" style="max-width: 400px;">
            >>> cat /home/wol/about.txt
            <br /><br />
            嗨👋，这里是 WoL 的主页。
            <br />
            🏳️‍⚧️+= | 初中生 | 👀 正在寻找开源项目 to collaborate on
            <br /><br />
            喜欢各种折腾，会玩各种编程语言。
            <br />
            (Network Security & Performance Developer, DDoS/CC Stresser? <del>CloudFlare 资深用户</del>)
            <br />
            虽然没有好的电脑，存储容量也小的可怜，但还是喜欢自己构建乱七八糟的东西 <del>(KernelSU-5.4.210 is the best)</del>。
            <br />
            仰望各界大佬。认识一下？
        </v-card-text>
    </v-card>
</template>

<script>
export default {
    props: {
        dark: {
            type: Boolean,
            required: true,
        },
    },
};
</script>