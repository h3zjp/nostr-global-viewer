<script setup lang="ts">
import { ref } from "vue";
const props = defineProps({
  isLogined: {
    type: Boolean,
    required: true,
  },
  login: {
    type: Function,
    required: true,
  },
});

// const nip07exists = ref('nostr' in window);
const nip07exists = true;
</script>
<template>
  <div class="p-index-intro" v-if="!props.isLogined">
    <h2 class="p-index-intro__head"><span>はじめに</span></h2>
    <p class="p-index-intro__text">Nostr を始めてみたくなった方は</p>
    <p class="p-index-intro__text">
      <a href="https://welcome.nostr-jp.org/" rel="noopener" target="_blank" class="p-index-intro__btn">Welcome to
        Nostr</a>
    </p>
    <p class="p-index-intro__text">をはじめに読んでみて下さい。<br />また、ちょっと詳しいことが気になった方は</p>
    <p class="p-index-intro__text">
      <a href="https://scrapbox.io/nostr/%E3%81%AF%E3%81%98%E3%82%81%E3%81%A6%E3%81%AENostr%E3%80%90%E3%81%AF%E3%81%98%E3%82%81%E3%81%A6%E3%81%AE%E6%96%B9%E3%81%AF%E3%81%93%E3%81%A1%E3%82%89%E3%80%91"
        rel="noopener" target="_blank" class="p-index-intro__btn">はじめてのNostr【はじめての方はこちら】</a>
    </p>
    <p class="p-index-intro__text">などを起点に調べてみると面白いと思います。</p>
    <h2 class="p-index-intro__head">このリレーについて</h2>
    <p class="p-index-intro__text">こちらのリレーは、日本国内からのみアクセスが可能なリレーとなります。(一部クラウド･VPN系ベンダー ASN 制限有)<br />
    </p>
    <p class="p-index-intro__text">このリレー宛に呟くと、廃人ランキングに自動参加されます。<br />
      ランキングはこちらから：<a href="https://nostr-ranking.h3z.jp/" target="_blank" rel="noopener">のす廃ランキング</a>
    </p>
    <p class="p-index-intro__text">
      サーバーについて詳しくは、<a href="https://hm-nrm.h3z.jp/apps-server/nostr.php" class="p-index-intro__text-link"
        target="_blank" rel="noopener">https://hm-nrm.h3z.jp/apps-server/nostr.php</a> をご覧下さい。
    </p>
    <h2 class="p-index-intro__head">ライセンス、ソースコードなど</h2>
    <p class="p-index-intro__text">このサイトのソースコードは<a href="https://github.com/h3zjp/nostr-global-viewer"
        class="p-index-intro__text-link" target="_blank">GitHub</a>にあります。
    </p>
    <p class="p-index-intro__text">
      <a href="https://awayuki.github.io/emojis.html" target="_blank" class="p-index-intro__text-link">SUSHIYUKI
        emojis (©awayuki)</a> の絵文字素材や
      <a href="https://soundeffect-lab.info/" target="_blank" class="p-index-intro__text-link">効果音ラボ</a>
      の効果音素材を利用しています。
    </p>
  </div>
</template>
<style scoped lang="scss">
.p-index-signin {
  background: rgba(0, 0, 0, 0.6);
  border-radius: 6px;
  padding: 12px;
  display: flex;
  align-items: center;
  gap: 10px;
  margin-top: 1rem;

  &__head {
    color: #ffffff;
    font-size: 14px;
  }

  &__body {
    flex-grow: 1;
    border-left: 1px solid #fff;
    padding-left: 10px;
  }

  &__btn {
    background-color: #fc5fa1;
    color: #ffffff;
    display: block;
    width: 100%;
    box-sizing: border-box;
    padding: 0.5rem 1.4rem;
    border-radius: 2rem;
    transition: all 0.4s;
    border: none;
    line-height: 1;
    cursor: pointer;

    &:hover {
      background-color: #df3d81;
    }
  }
}

.p-index-intro {
  margin-top: 2rem;

  @media screen and (max-width: 880px) {
    margin-top: 0rem;
  }

  &__head {
    font-size: 1.4rem;
    color: gold;
    display: flex;
    gap: 0.4rem;
    align-items: center;
    margin: 2rem 0 1rem 0;

    &::before {
      content: "";
      flex-grow: 1;
      height: 2px;
      background-color: gold;
    }

    &::after {
      content: "";
      flex-grow: 1;
      height: 2px;
      background-color: gold;
    }

    span {
      width: max-content;
      flex-grow: 0;
      flex-shrink: 0;
    }
  }

  &__text {
    color: #ffffff;
    margin: 0;
    line-height: 1.8;
    margin-top: 0.3rem;
  }

  &__text-link {
    color: #fc5fa1;
    font-weight: bold;
  }

  &__text code {
    display: inline-block;
  }

  &__btn {
    background-color: #fc5fa1;
    color: #ffffff;
    display: block;
    padding: 0.5rem 1.4rem;
    border-radius: 2rem;
    transition: all 0.4s;
    line-height: 1;
    margin: 0 auto;
    width: max-content;
  }

  &__btn:hover {
    background-color: #df3d81;
  }
}

@media screen and (max-width: 880px) {
  .p-index-post--signin {
    padding: 12px 0;
  }
}
</style>