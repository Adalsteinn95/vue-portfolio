<template>
  <div class='home'>
    <vue-header />
    <h1>{{ header }}</h1>
    <vue-footer />
  </div>
</template>

<script>
import Footer from "@/components/footer";
import Header from "@/components/header";

export default {
  name: "home",
  data() {
    return {
      header: "Welcome to Your Vue.js App",
      cv: {
        about: "Young computer science student looking for a future job",
        education: [
          {
            year: "2015-2018",
            school: "University of Iceland",
            subject: "BSc computer science"
          },
          {
            year: "2011-2015",
            school: "Menntaskólinn við Sund",
            subject: "Stúdentspróf"
          }
        ],
        experience: [
          {
            year: "2017-2018",
            work: "Teaching Assistant in University of Iceland"
          },
          {
            year: "2013-2017",
            work: "Librarian in Library of Kópavogur"
          }
        ],
        referrals: [
          {
            name: "Ólafur Sverrir Kjartansson",
            position: "adjunct",
            contact: "osk1@hi.is"
          },
          {
            name: "Lísa Z. Valdimarsdóttir",
            position: "Director of Bókasafn Kópavogs",
            contact: "lisa@kopavogur.is"
          }
        ]
      }
    };
  },
  components: {
    vueHeader: Header,
    vueFooter: Footer
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
