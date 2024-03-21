<script>
import SongsList from '@/components/SongsList.vue';

export default {
  components: {
    SongsList
  },
  data() {
    return {
      SongsList: [
        {
          id: 1,
          cover: '/papin_olimpos.png',
          title: 'Зомби по имени Билли',
          author: 'Папин Олимпос',
          audio: '/Papin_Olimpos_-_Zombi_po_imeni_Billi.mp3'
        },
        {
          id: 2,
          cover: '/give_tank.png',
          title: 'Маленький',
          author: 'Дайте танк (!)',
          audio: '/Dajjte_tank_-_Malenkijj_64714984.mp3'
        },
        {
          id: 3,
          cover: '/korol_and_shut.png',
          title: 'Кукла колдуна',
          author: 'Король и Шут',
          audio: '/Korol_i_SHut_-_Kukla_kolduna_62570545.mp3'
        },
        {
          id: 4,
          cover: '/stopban.png',
          title: 'мираж',
          author: 'STOPBAN',
          audio: '/stopban_-_mirazh_77049451.mp3'
        }
      ]
    }
  }
}
</script>

<template>
  <main class="main">
    <SongsList 
      :songsList="SongsList"
    />
  </main>
</template>
