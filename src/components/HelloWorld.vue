<script setup>
import Header from "./typography/Header.vue"
import Link from "./Link.vue"
import VueEasyLightbox from 'vue-easy-lightbox'
import {reactive} from "vue"
defineProps({
  msg: {
    type: String,
    required: true
  },
  bg: {
    type: String,
    required: false
  }
})
var imgs=["/Strahd.jpg"]
var state=reactive({open:false})
function togglegalery(){
  state.open=!state.open
}
</script>

<template>
  <div class="greetings">
    <Header text="Curse of Strahd">
    </Header>
    <div @click="togglegalery()">
    <img src="/Strahd.jpg">
    </div>
    <vue-easy-lightbox
      escDisabled
      moveDisabled
      :visible="state.open"
      :imgs="imgs"
      @hide="togglegalery"
    ></vue-easy-lightbox>
    <Link
      url="https://notebook-alex.notion.site/Super-Coole-D-D-Kampagne-a061e895c8d442d39b71c2fc6c77bd6d"
      text="Alex sein nices Dingens"
      >
    </Link>
  </div>
</template>