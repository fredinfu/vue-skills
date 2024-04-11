<template>
  <div class="holder">
    <form @submit.prevent="add">
    <input type="text" placeholder="Enter a skill you have.." v-model="skill" >
    </form>
    <ul>
      <li v-for="(data, index) in skills" :key="index">{{ data.Skill }}</li>
    </ul>
    <p>These are the skills that you possess.</p>
    <!-- <p v-if="skills.length>1">You have more than 1 skills</p>
    <p v-else>You have less than or equal to 1 skill</p>

    <div v-bind:class="{ alert: showAlert, another : showClass }"></div> -->
  </div>
</template>

<script>
export default {
  name: 'SkillsComponent',
  data() {
    return {
      skill: '',
      skills: [
        { "Skill": "Vue.js"},
        { "Skill": "Frontend Developer"}
      ]
    }
  },
  methods: {
  addSkill(event) {
    if (event.keyCode === 13) {
      // Aquí se ejecuta la acción deseada al presionar Enter
      // Ejemplo: agregar la habilidad a una lista
      this.skills.push({'Skill': this.skill});           
      this.skill = ""; // Limpiar el input
    }
  },
  add(){
    var skill = {Skill: this.skill};
    console.log(skill);
    this.skills.push(skill);
    this.skill = "";
  }

}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style >
  .holder {
    background: #fff;
  }

  ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
  }

  ul li {
    padding: 20px;
    font-size: 1.3m;
    background-color: #E0EDF4;
    border-left: 5px solid #3EB3F6;
    margin-bottom: 2px;
    color: #3E5252;
  }

  p {
    text-align: center;
    padding: 30px 0;
    color: gray;
  }

  .container {
    box-shadow: 0px 0px 40px lightgray;
  }

  input {
    width: calc(100% - 40px);
    border: 0;
    padding: 20px;
    font-size: 1.3m;
    background-color: #323333;
    color: #687F7F;
  }
</style>
