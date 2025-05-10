<template>
    <section id="skills" class="skills">
      <div class="container">
        <h2 class="section-title">Mes Compétences</h2>
        <div class="skills-container">
          <div class="skills-category">
            <h3>Frontend</h3>
            <div class="skills-grid">
              <div class="skill-card" v-for="(skill, index) in frontendSkills" :key="'front-'+index">
                <div class="skill-icon">
                  <i :class="skill.icon"></i>
                </div>
                <span class="skill-name">{{ skill.name }}</span>
              </div>
            </div>
          </div>
          <div class="skills-category">
            <h3>Backend</h3>
            <div class="skills-grid">
              <div class="skill-card" v-for="(skill, index) in backendSkills" :key="'back-'+index">
                <div class="skill-icon">
                  <i :class="skill.icon"></i>
                </div>
                <span class="skill-name">{{ skill.name }}</span>
              </div>
            </div>
          </div>
          <div class="skills-category">
            <h3>Outils & autres</h3>
            <div class="skills-grid">
              <div class="skill-card" v-for="(skill, index) in otherSkills" :key="'other-'+index">
                <div class="skill-icon">
                  <i :class="skill.icon"></i>
                </div>
                <span class="skill-name">{{ skill.name }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Skills',
    data() {
      return {
        frontendSkills: [
          { name: 'HTML5', icon: 'fab fa-html5' },
          { name: 'CSS3', icon: 'fab fa-css3-alt' },
          { name: 'JavaScript', icon: 'fab fa-js' },
          { name: 'Vue.js', icon: 'fab fa-vuejs' },
          { name: 'React', icon: 'fab fa-react' },
          { name: 'Sass', icon: 'fab fa-sass' },
          { name: 'Next.js', icon: 'fas fa-forward' }, // Icône améliorée
          { name: 'Bootstrap', icon: 'fab fa-bootstrap' },
        ],
        backendSkills: [
          { name: 'Node.js', icon: 'fab fa-node-js' },
          { name: 'Express', icon: 'fas fa-server' },
          { name: 'MongoDB', icon: 'fas fa-database' },
        ],
        otherSkills: [
          { name: 'Git', icon: 'fab fa-git-alt' },
          { name: 'GitHub', icon: 'fab fa-github' },
          { name: 'Figma', icon: 'fab fa-figma' },
          { name: 'Postman', icon: 'fas fa-paper-plane' }, // Icône améliorée
          { name: 'NPM', icon: 'fab fa-npm' },
          { name: 'VS Code', icon: 'fas fa-code' }
        ]
      }
    }
  }
  </script>
  
  
  <style scoped lang="scss"> 
  .skills {
    background-color: var(--dark-color);
    .section-title{
      color: var(--light-color);
    }
  }
  
  .skills-container {
    display: flex;
    flex-direction: column;
    gap: 50px;
  }
  
  .skills-category h3 {
    font-size: 1.5rem;
    margin-bottom: 30px;
    color: var(--light-color);
    text-align: center;
  }
  
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
    gap: 20px;
    justify-items: center;
    align-items: center;
  }
  
  .skill-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    padding: 10px;
    border-radius: 10px;
    transition: all 0.3s ease;
    background-color: var(--light-color);
    overflow: hidden;
    
  }
  
  .skill-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
    color: white;
  }
  
  .skill-card:hover .skill-icon {
    transform: scale(1.1);
  }
  
  .skill-card:hover .skill-name {
    color: white;
  }
  
  .skill-icon {
    font-size: 2.5rem;
    margin-bottom: 15px;
    transition: all 0.3s ease;
  }
  
  .skill-icon i {
    background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
  }
  
  .skill-card:hover .skill-icon i {
  background: white;
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  transform: rotate(360deg);
  transition: transform 0.5s ease;
}
  
  .skill-name {
    font-weight: 500;
    text-align: center;
    color: var(--dark-color);
    transition: color 0.3s ease;
  }
  
  @media (max-width: 768px) {
    .skills-grid {
      grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
      gap: 15px;
    }
    
    .skill-icon {
      font-size: 2rem;
    }
    
    .skill-name {
      font-size: 0.9rem;
    }
  }
  </style>