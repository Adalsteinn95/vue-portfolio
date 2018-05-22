<template>
  <div class='home'>
    <vue-header v-bind:title="header" v-bind:about="cv.about"/>
    <div class='educations'>
      <div v-for="education in cv.education" :key="education.year">
        <vue-education v-bind:data="education"/>
      </div>
    </div>
    <div class='projects'>
      <div v-for="project in cv.projects" :key="project.title">
        <vue-project v-bind:data="project"/>
      </div>
    </div>
    <div class='experience'>
      <div v-for="experience in cv.experience" :key="experience.year">
        <vue-experience v-bind:data="experience" />
      </div>
    </div>
    <div class='referrals'>
      <div v-for="referral in cv.referrals" :key="referral.name">
        <vue-referrals v-bind:data="referral" />
      </div>
    </div>
    <div class="skills">
      <div v-for="skill in cv.programmingLang" :key="skill.name">
        <vue-skills v-bind:data="skill" />
      </div>
    </div>
    <div class="other">
      <div v-for="item in cv.Other" :key="item.header">
        <vue-other v-bind:data="item" />
      </div>
    </div>
    <vue-footer v-bind:about="cv.about" />
  </div>
</template>

<script>
import Footer from "@/components/footer";
import Header from "@/components/header";
import Project from "@/components/project";
import Education from "@/components/education";
import Experience from "@/components/experience";
import Referrals from "@/components/referrals";
import Other from "@/components/other";
import Skills from "@/components/skills";

export default {
  name: "home",
  data() {
    return {
      header: "Aðalsteinn Ingi Pálsson",
      cv: {
        about: {
          description:
            "Young full stack programmer looking out for all the new things in programming!",
          email: "adalsteinn95@gmail.com",
          github: "https://github.com/adalsteinn95",
          linkedIn:
            "https://www.linkedin.com/in/a%C3%B0alsteinn-ingi-p%C3%A1lsson/",
          phonenumber: 8484830,
          address: "Breiðavík 13",
          city: "Reykjavik",
          country: "Iceland"
        },
        projects: [
          {
            title: "Weather Wherever",
            about:
              "It's a weather site made with NodeJs and plain javascript and CSS on the frontend. We host it through Heroku and we use Google maps API and Dark sky API.",
            repo: "https://github.com/weatherwherever/Weather"
          },
          {
            title: "KewlKwiz",
            about:
              "It's a website project that me and my friends did in school.We created a Restful API with Spring(java framework) and React as the Frontend.",
            repo: "https://github.com/CodeFriendsHI/React-Redux-Spring-Project"
          }
        ],
        education: [
          {
            year: "2015-present",
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
        ],
        programmingLang: [
          {
            name: "Javascript",
            description:
              "Has been my main programming language. I have used it In most of my projects wether it is an website, app, API and more. I have also been using some of the frameworks, mostly React"
          },
          {
            name: "Java",
            description:
              'Is the first programming language that I learned.I have done many projects in it. I like the "object oriented" thinking.'
          },
          {
            name: "Python",
            description: "Mostly used it when I am working with data."
          }
        ],
        Other: [
          {
            header: "Web and software development",
            items: ["React", "NodeJs", "NPM", "SCSS", "Spring", "Github"]
          },
          {
            header: "Cloud",
            items: ["Heroku", "AWS"]
          },
          {
            header: "OS",
            items: ["Linux", "Z-shell", "Tmux"]
          },
          {
            header: "Editors",
            items: ["Visual Code", "Atom", "Vim"]
          },
          {
            header: "Databases",
            items: ["PostgreSQL", "MySQL"]
          }
        ],
        basicLang: ["SQL", "C", "C++", "Scheme"]
      }
    };
  },
  components: {
    vueHeader: Header,
    vueFooter: Footer,
    vueProject: Project,
    vueEducation: Education,
    vueOther: Other,
    vueReferrals: Referrals,
    vueExperience: Experience,
    vueSkills: Skills,
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
