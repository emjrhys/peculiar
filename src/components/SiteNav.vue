<template lang='pug'>
div
  nav.sitenav.left
    a(href='https://open.spotify.com/artist/7sO3BcevkIUXu5NcUNBVfO?si=NRbFDvtGQEamdtZdjQQk7Q', target='_blank') Spotify
    a(href='https://www.facebook.com/modestaband/', target='_blank') Facebook
    a(href='https://soundcloud.com/modestaband', target='_blank') SoundCloud
  nav.sitenav.right
    a(href='https://twitter.com/modestaband', target='_blank') Twitter
    a(href='https://www.instagram.com/modestaband/', target='_blank') Instagram
    a(href='https://www.look-up-records.com/blog/2018/1/8/review-vhs-by-modesta', target='_blank') News
</template>

<script>
export default {
  name: 'SiteNav'
}
</script>

<style lang='scss'>
@import '../scss/_variables';

.sitenav {
  position: absolute;
  display: flex;
  justify-content: center;

  width: 100vh;
  height: 4rem;
  line-height: 4rem;
  top: calc(100% - 4rem);
  left: 4rem;

  transform: rotate(-90deg);
  transform-origin: 0 100%;
  
  z-index: 1000;

  perspective: 1000px;

  a {
    color: $black;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 1px;

    cursor: pointer;

    &:hover {
      opacity: .75;
    }

    & + a {
      margin-left: 1.5rem;
    }
  }

  &.right {
    transform: rotate(90deg);
    transform-origin: 100% 0;
    top: 100%;
    left: auto;
    right: 0;
  }
}
</style>
