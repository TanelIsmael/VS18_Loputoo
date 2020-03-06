<template>
  <div class="student">
    <Header></Header>
    <main>
      <h1 class="headline">Õpetaja</h1>
      <h2 class="sub-headline">Noorem tarkvaraarendaja</h2>
      <Tabs :tabs="tabs" :initialTab="initialTab">
        <template v-slot:tab-head-teadaanded>
          <p>Teadaanded</p>
        </template>
        <template v-slot:tab-panel-teadaanded>
          <textarea placeholder="Teadaanded õpilastele">

          </textarea>
          <input type="button" value="Saada teade">
        </template>
        <template v-slot:tab-head-taotlusleht>
          <p>Taotlusleht</p>
        </template>
        <template v-slot:tab-panel-taotlusleht>
          <div>
            <p>Praktikataotlus</p>
            <div class="buttons">
              <a href="#">Muuda</a>
              <a href="#">Täida taotlus</a>
            </div>
          </div>
        </template>
        <template v-slot:tab-head-hinnanguleht>
          <p>Hinnanguleht</p>
        </template>
        <template v-slot:tab-panel-hinnanguleht>
          <div>
            <p>Noorem tarkvaraarendaja 1. kursuse praktikajuhend</p>
             <div class="buttons">
              <a href="#">Muuda</a>
              <a href="#">Lae alla</a>
             </div>
          </div>
          <div>
            <p>Noorem tarkvaraarendaja 2. kursuse praktikajuhend</p>
            <div class="buttons">
              <a href="#">Muuda</a>
              <a href="#">Lae alla</a>
            </div>
          </div>
        </template>
        <template v-slot:tab-head-dokumendid>
          <p>Dokumendid</p>
        </template>
        <template v-slot:tab-panel-dokumendid>
          <div>
            <p>Praktikaprotsessi ülevaade</p>
            <a href="#">Halda</a>
          </div>
          <div>
            <p>Praktika tingimused ja kord</p>
            <a href="#">Halda</a>
          </div>
          <div>
            <p>Praktikaperioodid</p>
            <a href="#">Halda</a>
          </div>
          <div>
            <p>Välispraktika</p>
            <a href="#">Halda</a>
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
            <a href="#">Halda</a>
          </div>
          <div>
            <p>Praktika meelespea</p>
            <a href="#">Halda</a>
          </div>
          <div>
            <p>Hiljem praktikale mineku taotlus</p>
            <a href="#">Lae alla</a>
          </div>
          <div>
            <p>Kirjalike tööde vormistamisjuhend</p>
            <a href="#">Halda</a>
          </div>
          <div>
            <p>Praktika meelespea</p>
            <a href="#">Halda</a>
          </div>
          <div>
            <p>Praktikaaruande koostamise juhend</p>
            <a href="#">Halda</a>
          </div>
          <div>
            <p>Tööohutus- ja töötervishoiualane meelespea</p>
            <a href="#">Halda</a>
          </div>
        </template>
        <template v-slot:tab-head-opilased>
          <p>Õpilased</p>
        </template>
        <template v-slot:tab-panel-opilased>
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
        <template v-slot:tab-head-arhiiv>
            <p>Arhiiv</p>
        </template>
        <template v-slot:tab-panel-arhiiv>
            <div>
                <p>Õpilase nimi</p>
                <p>Kursus</p>
                <p>Praktikakoht</p>
                <p>Praktikaperiood</p>
                <a href="#">Dokumendid</a>    
            </div>
        </template>
      </Tabs>
    </main>
    <Footer></Footer>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header';
import Tabs from '@/components/Tab/Tabs';
import Footer from '@/components/Footer';

export default {
  name: 'student',
  components: {
    Header,
    Tabs,
    Footer
  },
  data() {
    return {
      initialTab: 'teadaanded',
      tabs: ['teadaanded', 'taotlusleht', 'hinnanguleht', 'dokumendid', 'abimaterjalid', 'õpilased', 'arhiiv']
    }
  }
}
</script>



<style lang="scss" scoped>
  .student {
    // display: flex;
    // flex-direction: column;
    // justify-content: space-evenly;


    main {
      padding: 5rem 15rem;
      margin-bottom: 108px;
    }

    .headline {
      font-family: 'Source Sans Pro', sans-serif;
      font-weight: 700;
      color: #404040;
      font-size: 2.25rem;
      margin-bottom: 20px;
    }

    .sub-headline {
        font-family: 'Open Sans', sans-serif;
        font-size: 24px;
        color: #404040;
        font-weight: 400;
        line-height: 38.4px;
        margin-bottom: 15px;
    }
  }
</style>