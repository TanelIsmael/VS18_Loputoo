<template>
    <Tabs :tabs="tabs" :initialTab="initialTab">
        <template v-slot:tab-head-taotlusleht>
          <p>Taotlusleht</p>
        </template>
        <template v-slot:tab-panel-taotlusleht>
          <div>
            <p>Praktikataotlus</p>
            <a href="#">Täida taotlus</a>
          </div>
        </template>
        <template v-slot:tab-head-hinnanguleht>
          <p>Hinnanguleht</p>
        </template>
        <template v-slot:tab-panel-hinnanguleht>
          <div>
            <p>Noorem tarkvaraarendaja 1. kursuse hinnanguleht</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Noorem tarkvaraarendaja 2. kursuse hinnanguleht</p>
            <a href="#">Lae alla</a>
          </div>
        </template>
        <template v-slot:tab-head-juhendid>
          <p>Juhendid</p>
        </template>
        <template v-slot:tab-panel-juhendid>
          <div>
            <p>Noorem tarkvaraarendaja 1. kursuse praktikajuhend</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Noorem tarkvaraarendaja 2. kursuse praktikajuhend</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Kirjalike tööde vormistamise juhend</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Praktika aruande koostamise juhend</p>
            <a href="#">Lae alla</a>
          </div>
        </template>
        <template v-slot:tab-head-dokumendid>
          <p>Dokumendid</p>
        </template>
        <template v-slot:tab-panel-dokumendid>
          <div>
            <p>Praktikaprotsessi ülevaade</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Praktikaperioodid</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Praktilise töö ning praktika läbiviimise tingimused ja kord Tartu Kutsehariduskeskuses</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>STARR analüüs</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>STARR tehnika analüüs</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Praktika arvestamine VÕTA-ga</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Välispraktika</p>
            <a href="#">Lae alla</a>
          </div>
        </template>
        <template v-slot:tab-head-abimaterjalid>
          <p>Abimaterjalid</p>
        </template>
        <template v-slot:tab-panel-abimaterjalid>
          <div>
            <p>Praktika äpp</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Praktikakohad</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Praktika meelespea</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Hiljem praktikale mineku taotlus</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Tööohutus- ja töötervishoiualane meelespea</p>
            <a href="#">Lae alla</a>
          </div>
        </template>
      </Tabs>
</template>

<script>
import Tabs from '@/components/Tab/Tabs.vue'

export default {
    name: 'Tab',
    data() {
        return {
            initialTab: 'taotlusleht',
            tabs: ['taotlusleht', 'hinnanguleht', 'juhendid', 'dokumendid', 'abimaterjalid']
        }
    },
    components: {
        Tabs
    }
}
</script>