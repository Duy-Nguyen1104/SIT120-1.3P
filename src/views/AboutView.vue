<template>
  <div class="about-me">
    <div class="left-column">
      <h2>About Me</h2>
      <p>As an enthusiastic and dedicated student majoring in IT, I am confident that I 
        could bring valuable assets to the company with my skillsets. Throughout my academic journey, 
        I have honed my skills in web appplication development, and I am eager to apply my knowledge in 
        the real-world.
      </p>
      <p>
        What sets me apart from other candidates is my ability to adapt to evolving technologies and trends
        within the web development landscape. Not only that, I am a proactive learner who strive to learn new
        skills to make myself as versatile and handy as possible.
      </p>
    </div>

    <div class="right-column">
      <h2>Skills</h2>
      <table class="skills-table">
        <thead>
          <tr>
            <th>Programming Language</th>
            <th>Proficiency</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(language, proficiency) in programmingLanguages" :key="language">
            <td>{{ language }}</td>
            <td>{{ proficiency }}</td>
          </tr>
        </tbody>
      </table>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      programmingLanguages: {
        HTML: "Advanced",
        Python: "Intermediate",
        JavaScript: "Advanced",
        Java: "Intermediate",
      },
    };
  },
};
</script>

<style scoped>
.about-me {
  max-width: 1300px;
  margin: 0 auto;
  padding: 20px;
  font-family: Arial, sans-serif;
  display: flex;
  flex-direction: row;
  background-color: white;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.left-column,
.right-column {
  flex: 1;
  padding: 0 20px; /* Added padding for both columns */
}

p {
  font-size: 20px;
}

.skills-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 10px;
}

.skills-table th,
.skills-table td {
  border: 1px solid #ccc;
  padding: 10px;
  text-align: center;
}

.skills-table th {
  background-color: #f0f0f0;
  font-weight: bold;
}

.skills-table td {
  background-color: #fff;
}
</style>
