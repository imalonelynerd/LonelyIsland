<script setup>

import CellCluster from "@/components/cellClusters/CellCluster.vue";
import {ref} from "vue";
import nestedPath from "@/assets/json/nestedPath.json";
import {changeLoc, copyText, mailTo} from "@/assets/js/menuUtils";

const contact = ref({
  links: [
    {
      onc: function () {
        copyText('imalonelynerd')
      },
      img: `${nestedPath.path}icons/socials/discord.webp`,
      title: "Discord",
      span: "imalonelynerd",
      style: "#5D76FF"
    },
    {
      onc: function () {
        mailTo("mailto:imalonelynerd@gmail.com");
      },
      img: `${nestedPath.path}icons/socials/mail.webp`,
      title: "Mail",
      span: "imalonelynerd@gmail.com",
    },
    {
      onc: function () {
        changeLoc("https://github.com/imalonelynerd/");
      },
      img: `${nestedPath.path}icons/socials/github.webp`,
      title: "GitHub",
      span: "imalonelynerd",
      style: "#202020"
    },
    {
      onc: function () {
        changeLoc("https://mastodon.social/@imalonelynerd/");
      },
      img: `${nestedPath.path}icons/socials/mastodon.webp`,
      title: "Mastodon",
      span: "@imalonelynerd@mastodon.social",
      style: "#6364FF"
    },
    {
      onc: function () {
        changeLoc("https://reddit.com/u/smpl_deb");
      },
      img: `${nestedPath.path}icons/socials/reddit.webp`,
      title: "Reddit",
      span: "u/smpl_deb",
      style: "#FF5709"
    },
    {
      onc: function () {
        changeLoc("https://www.figma.com/@imalonelynerd");
      },
      img: `${nestedPath.path}icons/socials/figma.webp`,
      title: "Figma",
      span: "@imalonelynerd",
      style: "#202020"
    },
    {
      onc: function () {
        changeLoc("https://www.tumblr.com/imalonelynerd");
      },
      img: `${nestedPath.path}icons/socials/tumblr.webp`,
      title: "Tumblr",
      span: "imalonelynerd",
      style: "#266CBE"
    },
    {
      onc: function () {
        changeLoc("https://twitter.com/wormdramaVEVO");
      },
      img: `${nestedPath.path}icons/socials/twitter.webp`,
      title: "Twitter",
      span: "@wormdramaVEVO",
      style: "#24A3F1"
    },
    {
      onc: function () {
        changeLoc("https://heroes.imalonelynerd.fr/imalonelynerd");
      },
      img: `${nestedPath.path}icons/socials/prettyheroes.webp`,
      title: "PrettyHeroes",
      span: "imalonelynerd",
      style: "#FF5263"
    }
  ]
});

</script>

<template>
  <CellCluster :cellList="contact" listType="BlockList" shownTitle="Let's get in touch !"/>
</template>

<style scoped>
div {
  animation: Hewwo ease-out 0.75s;
}
</style>