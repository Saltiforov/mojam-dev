<template>
  <section id="item">
    <FirstScreen
      :title="firstScreen.title"
      :subtitle="firstScreen.subtitle"
      :buttonOrange="firstScreen.buttonOrange"
      :buttonDark="false"
      :background="firstScreen.background"
      :crumbsActive="firstScreen.crumbActive"
      :crumbs="firstScreen.crumbs"
      :bigScreen="false"
      :routeBtnOrange="firstScreen.routeBtnOrange"
    />
    <ItemInfo />
    <Bonus :homePage="false" />
    <Info />
    <Partner />
    <Summary />
  </section>
</template>
<script>
import FirstScreen from '@/components/Home/FirstScreen'
import ItemInfo from '@/components/Item/Info'
import Bonus from '@/components/Home/Bonus'
import Info from '@/components/Career/Info'
import Partner from '@/components/Career/Partner'
import Summary from '@/components/Career/SendSummary'
export default {
  data() {
    return {
      firstScreen: {
        title: 'UX/UI Designer/Art Director',
        subtitle: '$3000–4500',
        buttonOrange: 'Показать нам свое CV',
        background: '/career/background.png',
        crumbActive: 'Главная/ Карьера',
        crumbs: '/ UX/UI Designer/ Art Director',
        routeBtnOrange: '/',
      }
    }
  },
  components: {
    FirstScreen,
    Bonus,
    Info,
    Partner,
    Summary,
    ItemInfo
  }
}
</script>
<style lang="scss">

</style>
