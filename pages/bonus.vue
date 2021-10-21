<template>
  <section id="bonus__coop">
    <FirstScreen
      :title="firstScreen.title"
      :subtitle="firstScreen.subtitle"
      :buttonOrange="false"
      :buttonDark="false"
      :background="firstScreen.background"
      :crumbsActive="firstScreen.crumbActive"
      :crumbs="firstScreen.crumbs"
      :bigScreen="false"
      :routeBtnOrange="firstScreen.routeBtnOrange"
    />
    <Slider />
    <Bonus />
  </section>
</template>
<script>
import FirstScreen from '@/components/Home/FirstScreen'
import Slider from '@/components/BonusPage/CoopSlider'
import Bonus from '@/components/Home/Bonus'
export default {
  data() {
    return {
      firstScreen: {
        title: 'Команда — наша семья',
        subtitle: 'Мы не только хорошо работаем, но и классно отдыхаем',
        background: '/bonus/bg-bonus.png',
        crumbActive: 'Главная/',
        crumbs: ' Бонусы сотрудничества',
        routeBtnOrange: '/',
      }
    }
  },
  components: {
    FirstScreen,
    Bonus,
    Slider
  }
}
</script>
