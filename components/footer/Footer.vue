<template lang="pug">
footer.footer
  .wrapper
    .brand
      nuxt-link.logo(to="/")
        span.visually-hidden Vue mastery
        img(src="/images/lgo-vue-mastery-green.png" role="logo")
      p As the ultimate resource for Vue.js developers, Vue Mastery produces weekly lessons so you can learn what you need to succeed as a Vue.js Developer.
      .social
        a.button.primary.link.inverted.-has-icon(href='https://www.facebook.com/vuemastery' target="_blank")
          i.fab.fa-facebook
        a.button.primary.link.inverted.-has-icon(href='https://twitter.com/vuemastery' target="_blank")
          i.fab.fa-twitter
        a.button.primary.link.inverted.-has-icon(href='https://medium.com/vue-mastery' target="_blank")
          i.fab.fa-medium
        a.button.primary.link.inverted.-has-icon(href='https://www.youtube.com/vue-mastery' target="_blank")
          i.fab.fa-youtube
    .nav
      h4 Navigate
      ul.list-unstyled
        li
          nuxt-link(to='/courses' class="-inverted") Courses
        li
          nuxt-link(to='/about' class="-inverted") About
        li
          nuxt-link(to='/contact' class="-inverted") Contact
        li
          nuxt-link(to='/privacy' class="-inverted") Privacy Policy
        li
          nuxt-link(to='/terms' class="-inverted") Terms of Service
    //- .form-section
    //-   h4 Get notified when we release new lessons.
    //-   form.form
    //-     .form-group
    //-       label.visually-hidden Name
    //-       input(class="input primary -hollow" placeholder="Name")
    //-     .form-group
    //-       label.visually-hidden Email
    //-       input(class="input primary -hollow" placeholder="Email")
    //-     button(type="submit" class="button primary -small") Subscribe
</template>

<script>
export default {'name': 'Footer'}
</script>

<style lang="stylus" scoped>
@import '~assets/css/_variables'

.footer
  background-color $secondary-color
  color #fff
  padding ($vertical-space/2) 0
.wrapper
  display grid
  text-align center
  grid-template-columns 1fr
  grid-template-areas "nav"\
                      "brand"\
                      "form"

  +tablet-up()
    text-align left
    grid-template-columns 1fr 1fr
    grid-template-areas "brand nav"
    // grid-template-areas "brand nav ."\
    //                     "form . ."
  // +laptop-up()
  //   grid-template-columns 1fr 1fr 1fr
  //   grid-template-areas "brand nav form"

.brand
  grid-area brand
  margin-bottom ($vertical-space/2)

  .logo
    display block
    max-width 284px
    min-width 200px

    +mobile-only()
      margin: 45px auto

    img
      display block
      width 100%

.social
  display flex
  font-size 1.5em

.nav
  grid-area nav
  justify-self center

  h4
    text-transform uppercase

  li
    margin 15px 0

.form-section
  grid-area form

  .form
    display grid

    .button
      justify-self end

</style>
