<template>
  <div class="education">
    <School 
        name="Universiti Tunku Abdul Rahman"
        year="2018-2021"
        scholar="Degree"
        field="Software Engineering"
        result="CGPA 3.3759"
        :imgSrc="require('~/assets/images/UTAR.jpg')"
    />
    
    <School 
        name="Pei Hwa High School"
        year="2012-2017"
        scholar="UEC"
        field="Science Stream"
        result="5A 4B 1C"
        :imgSrc="require('~/assets/images/secondarySchool.jpg')"
    />
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