<template>
  <div class="education">
    <School 
        name="Universiti Tunku Abdul Rahman"
        year="2018-2021"
        scholar="Degree"
        field="Software Engineering"
        result="CGPA 3.3759"
        :imgSrc="require('~/assets/images/UTAR.jpg')"
    >
      <p>
        UTAR is the university that I chose to continue my study. The reason
        that I chose to study Software Engineering is because I am interested 
        in IT industries and also engineering. Before I start to study in UTAR, 
        I have heard about that the final examinations in UTAR are extraordinarily 
        hard and the assignments that need to be completed are quite heavy.
      </p>
      <p>
        Fortunately, I meet some nice and smart course mates at the beginning of 
        my study in UTAR. We work together to complete those heavy assignments 
        and sometimes burning midnight oils to deal with the numerous assignments. 
        Besides that, we also study and prepare ourselves together in UTAR campus 
        when the midterm or final examination is around the corner to get a better
        understanding on the things we learnt and try to obtain a better results.
      </p>
      <p>
        Throughout my entire university life, I have learnt a few of programming
        languages such as C++, C#, Java, Python, HTML, PHP, JavaScript, React-Native,
        Laravel and furthermore. Moreover, I also exposed to the knowledges regrading
        software development such as software design, software testing, software
        requirement, data structures, database system, software quality assurance,
        software constructions, software configurations and others which are important
        in Software Engineering programme.
      </p>
    </School>
    
    <School 
        name="Pei Hwa High School"
        year="2012-2017"
        scholar="UEC"
        field="Science Stream"
        result="5A 4B 1C"
        :imgSrc="require('~/assets/images/secondarySchool.jpg')"
    >
      <p>
        Pei Hwa High School is the secondary school that I studied from year 2012 to
        2017. It is an independent secondary school and considered as a small school.
        When I first get into the school, the student amount of the school are less
        than 300. However, the student amount are increasing year by year and more that
        500 after I graduated from it.
      </p>
      <p>
        Due to the great results I got in my UPSR, I received scholarship while study 
        in Pei Hwa High School. After completed the UEC Junior Middle level when I was
        15 years old, I chose Science Stream to further continue my study in secondary school.
        The interesting things during my secondary school life is that the total students 
        in science class is only 6. 
      </p>
      <p>
        In my secondary school life, I was active in the extracurricular activities and the
        society I joined is Scout. I learnt much knowledges besides books during my Scout life.
        Due to the efforts I put in my studies and extracurricular activities, I was awarded   
        Outstanding Student Awards(2016,2017) and Outstanding Society's Board of Directors 
        Award when I graduated.
      </p>
    </School>

  </div>
</template>

<script>
export default {
  head: () => ({
    title: 'Education',
  }),
};
</script>

<style lang="scss" scoped>
.education {
    display: flex;
    flex-direction: column;
}
</style>