<template>
    <article>
    <h2>A little about me</h2>
    <p>
      I'm a software engineer with a computer science background. I started my career as a front-end developer in a automobile 
      financing company owned by Volkswagen and transitioned into a full-stack role for a Swiss health-tech company. Working in the
      latter in an international remote context, made me understand the importance of effective communication and collaboration, 
      even across different time zones.
    </p>
    <p>
      Over the past four years, I have honed my skills in .NET and C#, crafting efficient and scalable solutions that meet client 
      needs. Additionally, my proficiency in Vue.js and TypeScript enables me to create dynamic and responsive front-end interfaces. 
      My dedication to staying updated with the latest technologies ensures that I am always equipped to tackle new challenges and 
      deliver high-quality results.
    </p>
    <p>
      I have a deep passion for traveling. Whenever I'm not working, I find myself exploring different countries and continents. 
      I'm also a big nerd for video games, technology, and reading books, which keep me my brain's neurons active. My main 
      hobby is photography, and I have plans to add a section to this website with a catalog of my pictures, capturing the essence 
      of the diverse places I visit and the moments I cherish.
    </p>
    <ul>
      <li>
        <img src="../assets/icons/net-core.svg" alt="netcore" />
      </li>
      <li>
        <img src="../assets/icons/csharp.svg" alt="csharp" />
      </li>
      <li>
        <img src="../assets/icons/vue.svg" alt="vuejs" />
      </li>
      <li>
        <img src="../assets/icons/typescript.svg" alt="typescript" />
      </li>
      <li>
        <img src="../assets/icons/sql.svg" alt="sql" />
      </li>
      <!--<li>
        <a :href="pdf" download>
          <button>Resume</button>
        </a>
      </li>-->
    </ul>
  </article>
</template>

<script>
export default {
  name: "Description",
  data() {
    return {
      pdf: require("../assets/files/cv_DuarteVital.pdf"),
    };
  },
}
</script>

<style scoped>
  p {
  font-size: clamp(16px, 1.15vw, 1.15vw);
  line-height: 2;
  color: #9d9d9d;
}

h2 {
  font-size: clamp(24px, 3vw, 3vw);
  font-weight: 300;
  margin: 0;
}

ul {
  margin-top: clamp(3em, 4vw, 4vw);
  list-style-type: none;
  display: flex;
  justify-content: space-around;
}

img {
  height: 40px;
  filter: grayscale();
  transition: filter 0.2s ease-in-out;
}

button {
  height: 30px;
  border: none;
  outline: none;
  font-size: 18px;
  font-weight: 900;
  background-color: white;
  cursor: pointer;
  transition: background-color 0.2s ease-in-out;
}

button:hover {
  background-color: var(--primary-color);
  ;
}

img:hover {
  filter: none;
}

span {
  background-color: #141414;
  margin: 0.3em;
  padding: 0.3em 0.7em;
  color: #8d8d8d;
}

@media (max-width: 700px) {

  img,
  button {
    height: 20px;
  }
}
</style>