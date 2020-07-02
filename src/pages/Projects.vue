<template>
  <div id="page">
    <h2 class="subTitle">Projects</h2>
    <div id="projects">
      <div class="project">
        <div class="projectTitle"><h2 class="projectTitle">EduBot</h2></div>
        <div>
          <div class="projectText">
            <p>Key Stage 3 students are now required to learn basic programming concepts, including looping, functions, sorting and searching. However, a lack of fully qualified Computing teachers has made it very difficult for some schools to meet the curriculum requirements. Which means many students are missing out on crucial programming education.</p>
            <p>We (a team of four) designed EduBot to help solve this problem. After being given a textual introduction to a programming concept, students attempt to implement an algorithm using code blocks which will make a robot move around a level. The goal is make EduBot gather all the nuts and bolts in as few moves as possible. Each level provides the student with a new challenge and a new programming concept to master. The platform also provides teachers with the ability to track their students' progress and to give feedback to individual students on each level.</p>
            <p>EduBot ranked in the top 5 projects in our year group (out of over 40 projects) and our team was invited to present EduBot at the department's open day.</p>
          </div>
          <div class="projectPicDiv">
            <img class="projectPic" src="../assets/edubot.png"/>
          </div>
        </div>
      </div>
      <div class="project">
        <div class="projectTitle"><h2 class="projectTitle">Genetic Search</h2></div>
        <div>
          <p>A library for building and running genetic algorithms and evolutionary strategies.</p>
          <p>As a brief introduction: a genetic algorithm consists of a population - a set of genotypes, each genotype can be thought of as the encoding of some property. A genetic algorithm's goal is to find the genotype(s) with the highest fitness (this is something which needs to be defined by the user). To do this the algorithm works iteratively; on each iteration it takes some of the fitter genotypes and mutates them in some way, adds these new genotypes to the population and removes genotypes with lower fitness. The algorithm continues to do this until the maximum number of iterations are reached or until some condition is met.</p>
          <p>This library aims to be highly customisable (yet still user-friendly) and so I decided to represent each genotype as a list of floating point numbers, this allows users to write both evolutionary strategies and traditional genetic algorithms. Each stage in the genetic algorithm cycle can be customised, for example fitness evaluation, mutation, selection, etc. The library provides a number of common operators, rather than the user always having to write their own. The library also makes use of multi-threading; passing off jobs to an executor where operators are applied to individual genotypes.</p>
        </div>
      </div>
      <div class="project">
        <div class="projectTitle"><h2 class="projectTitle">Genetipher</h2></div>
        <div>
          <p>A tool which uses <b>genetic</b> algorithms to solve substitution <b>ciphers</b> (in fact it uses the genetic search library above).</p>
          <p>The most interesting part of this project is giving each possible decoding (each genotype) a fitness score. To do this I decode the ciphertext using a genotype, then split the decoded text into tri-grams (sequences of three characters) and score the genotype based on the number of times the tri-grams appear in a pre-processed corpus of English text. This should give a good indication of how closely the decoded text resembles English.</p>
          <p>At the moment the project can decipher a 230 word message in around 50 seconds, however the English isn't always 100% accurate; sometimes some letters get mixed up. I hope to improve the accuracy and speed of the deciphering in the near future. There are a number of new features I would like to add as well. For example, being able to solve other types of cipher, not just substitution, and being able to search for the correct type of cipher if it is not known beforehand.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "projects"
  }
</script>

<style scoped>
.subTitle {
  /*font-family: 'Merriweather', serif;*/
  font-family: Oswald, sans-serif;
  font-size: 30px;
  font-weight: bold;
  border-bottom: 1px lightgrey solid;
  color: palevioletred;
}
.project {
  /*font-family: 'Merriweather', serif;*/
  border: 1px lightgrey solid;
  font-family: Nunito, sans-serif;
  border-radius: 10px;
  padding: 20px;
  display: block;
  margin: 40px 0px;
}
.projectTitle {
  font-family: Oswald, sans-serif;
  margin: 5px 0px 10px 0px;
  font-size: 28px;
}
.projectPicDiv {
  padding-top: 10px;
  width: 100%;
  display: flex;
  justify-content: center;
}
.projectPic {
  width: 75%;
  height: 75%;
  border: 1px lightgrey solid;
  border-radius: 5px;
}
</style>
