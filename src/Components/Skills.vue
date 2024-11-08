<template>
  <div class="skills-container max-w-4xl mx-auto py-12 px-6 bg-gray-50 rounded-lg shadow-lg">
    <h2 class="text-3xl font-bold text-center mb-8 text-blue-600">
      Group Skills
    </h2>
    <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4">
      <div
        v-for="(skill, index) in skills"
        :key="index"
        class="skill-card flex items-center justify-center p-4 bg-white rounded-lg shadow-md hover:shadow-lg transition duration-300 transform hover:-translate-y-1"
      >
        <img :src="skill.img" :alt="skill.name" class="skill-icon" />
        <span class="text-lg font-semibold text-teal-600">{{ skill.name }}</span>
      </div>
    </div>
  </div>
</template>

<script>
import SqlImg from '../assets/sql.svg';
import ReactImg from '../assets/react.svg';
import VueImg from '../assets/vue.svg';
import VisualImg from '../assets/visual.svg';
import MongoDbImg from '../assets/mongo.svg';
import PostgresImg from '../assets/postgres.svg';
import NodeImg from '../assets/node.svg';
import PythonImg from '../assets/python.svg';
import JsImg from '../assets/js.svg';
import JavaImg from '../assets/java.svg';
import FigmaImg from '../assets/figma.svg';
import GitImg from '../assets/git.svg';
import HtmlCssImg from '../assets/html-css.svg';


export default {
  name: 'Skills',
  data() {
    return {
      skills: [
        { name: 'SQL', img: SqlImg },
        { name: 'React', img: ReactImg },
        { name: 'Vue.js', img: VueImg },
        { name: 'Node.js', img: NodeImg },
        { name: 'Python', img: PythonImg },
        { name: 'JavaScript', img: JsImg },
        { name: 'Java', img: JavaImg },
        { name: 'Figma', img: FigmaImg },
        { name: 'Git', img: GitImg },
        { name: 'HTML & CSS', img: HtmlCssImg },
        { name: 'PostgreSQL', img: PostgresImg },
        { name: 'Visual Studio', img: VisualImg },
      ]
    };
  }
};
</script>

<style scoped>
.skill-icon {
  width: 50px;
  height: 50px;
  object-fit: contain;
  margin-bottom: 10px;
}

.skill-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

h2 {
  font-size: 2rem;
  margin-bottom: 20px;
}
</style>
