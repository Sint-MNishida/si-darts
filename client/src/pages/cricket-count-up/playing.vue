<template>
  <playing-page v-bind="vbPlayingPage" />
</template>
<script lang="ts">
import { Component, mixins } from 'nuxt-property-decorator';

import BasePage from '~/components/pages/ContainerBase/PlayingBasePage';
import PlayingPage from '~/components/pages/CricketCountUp/PlayingPage.vue';

@Component({
  layout: 'playing',
  components: { PlayingPage },
})
export default class extends mixins<BasePage>(BasePage) {
  private get vbPlayingPage(): Partial<PlayingPage> {
    return {
      playerNum: this.playerNum,
      gameTitle: 'Cricket Count Up',
    };
  }
}
</script>
