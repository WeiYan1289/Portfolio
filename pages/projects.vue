<template>
  <div class="projects">
    <Project
        name="Shiganshima Online Clothes Retail Store"
        type="Web Application"
        year="2021"
        :imgSrc="require('~/assets/images/project1.png')"
        :lists="lists[0]"
    >
      <p>
        This is  a web application which build for a simple clothes retail store named 
        Shiganshima. This web application is built to practice the <span>role-based access 
        control (RBAC), authentication and authorization</span> in Laravel. Besides that, 
        it also built for me to  be more familiar with Laravel and it’s not make for 
        any commercial purpose.
      </p>
      <p>
        The CRUD operation in this web application are interacted within the database 
        in local machine. There are three roles in this web application which are member 
        customer, non-member customer and admin. The actions they can perform and 
        the views they can see are different depending to their roles.
      </p>
    </Project>

    <Project
        name="Personal Portfolio"
        type="Webpage"
        year="2021"
        :imgSrc="require('~/assets/images/project2.png')"
        :lists="lists[1]"
    >
      <p>
        This project is to construct my own <span>portfolio website</span> which is this current 
        website. This <span>portfolio website</span> shares my introduction and information, which
        are a brief introduction about myself, the education that I been went through,
        and also some projects that I did. The designs of this website have referred to 
        some awesome websites and followed my friend's advice who are talented in building
        beautiful website. This website will change its UI and views when the screen size
        is different.
      </p>
    </Project>

    <Project
        name="Profiling Student Performance in Projects Using Clustering"
        type="Final Year Project"
        year="2021"
        :imgSrc="require('~/assets/images/project3.png')"
        :lists="lists[2]"
    > 
      <p>
        This final year project is a <span>research-based project</span> which focusing on using data 
        mining techniques to analyse the students data in projects. This project was started
        by collecting the data then using Python and R to process the data for further 
        analysis. After that, Waikato Environment for Knowledge Analysis (WEKA) was used
        to carry out the clustering for reporting. 
      </p>
      <p>
        The main propose of this project is to assist lecturer on decision making while
        monitor different type of student in projects. The <span>data mining algorithms</span> are 
        applied to the dataset and analysis are completed to carry out the profiling of
        different types of students.
      </p> 
    </Project>  
  </div>
</template>

<script>
export default {
  head: () => ({
    title: 'My Projects',
  }),

  computed: {
    lists() {
      return [
        [
          {
            name: 'Laravel',
            imgSrc: `${require(`~/assets/images/logo/laravel.png`)}`,
          },
          {
            name: 'HTML',
            imgSrc: `${require(`~/assets/images/logo/html.png`)}`,
          },
          {
            name: 'CSS',
            imgSrc: `${require(`~/assets/images/logo/css.png`)}`,
          },
        ],
        [
          {
            name: 'Nuxt.js',
            imgSrc: `${require(`~/assets/images/logo/nuxt.svg`)}`,
          },
          {
            name: 'Vue.js',
            imgSrc: `${require(`~/assets/images/logo/vue.png`)}`,
          },
          {
            name: 'Vuetify',
            imgSrc: `${require(`~/assets/images/logo/vuetify.png`)}`,
          },
          {
            name: 'Sass',
            imgSrc: `${require(`~/assets/images/logo/sass.png`)}`,
          },
          {
            name: 'Node.js',
            imgSrc: `${require(`~/assets/images/logo/node.png`)}`,
          },
        ],
        [
          {
            name: 'Python',
            imgSrc: `${require(`~/assets/images/logo/python.png`)}`,
          },
          {
            name: 'R',
            imgSrc: `${require(`~/assets/images/logo/r.png`)}`,
          },
          {
            name: 'Jupyter Notebook',
            imgSrc: `${require(`~/assets/images/logo/jupyter.png`)}`,
          },
        ],
      ]
    }
  }
};
</script>

<style lang="scss" scoped>
.projects {
    display: flex;
    flex-direction: column;
}
</style>