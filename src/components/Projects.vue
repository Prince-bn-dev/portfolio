<template>
  <section id="projects" class="projects">
    <div class="container">
      <h2 class="section-title">Mes Projets</h2>
      <div class="projects-grid">
        <!-- Projet 1: By Ichola -->
        <div class="project-card" data-project="by-ichola">
          <div class="project-image">
            <img src="@/assets/images/by-ichola-preview.png" alt="By Ichola"/>
            <div class="project-links">
              <a href="https://by-ichola.vercel.app/" target="_blank" class="project-link">
                <i class="fas fa-eye"></i>
              </a>
              <a href="#" class="project-link" @click.prevent="showCaseStudy('byIchola')">
                <i class="fas fa-info-circle"></i>
              </a>
            </div>
          </div>
          <div class="project-info">
            <h3>By Ichola</h3>
            <p>Plateforme de Fast-food enlige avec le panier de commande</p>
            <div class="project-tags">
              <span>React</span>
              <span>Sass</span>
              <span>JavaScript</span>
            </div>
          </div>
        </div>

        <!-- Projet 2: FormCarry -->
        <div class="project-card" data-project="formcarry">
          <div class="project-image">
            <img src="@/assets/images/formcarry-preview.png" alt="FormCarry Frontend"/>
            <div class="project-links">
              <a href="https://formcarry-frontend-py8qj5rwm-princes-projects-aec51bab.vercel.app/" 
                 target="_blank" 
                 class="project-link">
                <i class="fas fa-eye"></i>
              </a>
              <a href="https://github.com/votre-user/formcarry-frontend" 
                 target="_blank" 
                 class="project-link">
                <i class="fas fa-code"></i>
              </a>
            </div>
          </div>
          <div class="project-info">
            <h3>FormCarry Frontend</h3>
            <p>Interface moderne pour service de gestion de formulaires avec analyse de données.</p>
            <div class="project-tags">
              <span>React 18</span>
              <span>Node.js</span>
              <span>MongoDB</span>
              <span>Express</span>
            </div>
          </div>
        </div>

        <!-- Projet 3: AdsPlane -->
        <div class="project-card" data-project="adsplane">
          <div class="project-image">
            <img src="@/assets/images/adsplane-preview.png" alt="AdsPlane"/>
            <div class="project-links">
              <a href="https://adsplane.com" target="_blank" class="project-link">
                <i class="fas fa-eye"></i>
              </a>
              <a href="#" class="project-link" @click.prevent="showCaseStudy('adsplane')">
                <i class="fas fa-chart-line"></i>
              </a>
            </div>
          </div>
          <div class="project-info">
            <h3>AdsPlane</h3>
            <p>Solution SaaS de gestion publicitaire avec tableau de bord analytique.</p>
            <div class="project-tags">
              <span>React</span>
              <span>Node.js</span>
              <span>MongoDB</span>
              <span>Express</span>
            </div>
          </div>
        </div>

        <!-- Projet 4: Ecomplane -->
        <div class="project-card" data-project="ecomplane">
          <div class="project-image">
            <img src="@/assets/images/ecomplane-preview.png" alt="Ecomplane"/>
            <div class="project-links">
              <a href="https://ecomplane.com" target="_blank" class="project-link">
                <i class="fas fa-eye"></i>
              </a>
              <a href="#" class="project-link" @click.prevent="showCaseStudy('ecomplane')">
                <i class="fas fa-users"></i>
              </a>
            </div>
          </div>
          <div class="project-info">
            <h3>Ecomplane (Collaboration)</h3>
            <p>Marketplace B2B pour fournisseurs africains avec système de dropshipping.</p>
            <div class="project-tags">
              <span>React </span>
              <span>NestJS</span>
              <span>MongoDB</span>
              <span>Express</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
  
  <script>
  export default {
    name: 'Projects',
    methods: {
    showCaseStudy(projectId) {
      // À implémenter : afficher une modale ou page dédiée
      console.log(`Voir étude de cas pour ${projectId}`);
      // this.$router.push(`/case-study/${projectId}`);
    }
  }
  }
  </script>
  <style scoped lang="scss">
  .project-card[data-project="adsplane"] {
  border-left: 4px solid #3a86ff;
}

.project-card[data-project="ecomplane"] {
  border-left: 4px solid #8338ec;
}

.project-card[data-project="by-ichola"] {
  border-left: 4px solid #ff006e;
}

.project-card[data-project="formcarry"] {
  border-left: 4px solid #fb5607;
}

.project-link i.fa-info-circle {
  color: #17c3b2;
}

.project-link i.fa-chart-line {
  color: #ff006e;
}

.project-link i.fa-users {
  color: #8338ec;
}
  .projects {
    background-color: var(--gray-color);

    .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
    gap: 30px;
      .project-card {
      background-color: white;
      border-radius: 10px;
      overflow: hidden;
      box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
         &:hover {
          transform: translateY(-10px);
          box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
          .project-image img {
            transform: scale(1.1);
          }
          .project-image .project-links {
            opacity:1 ;
          }

        };
         .project-image {
          position: relative;
          height: 250px;
          overflow: hidden;
           img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
          }
           .project-links {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 20px;
            background-color: rgba(58, 134, 255, 0.8);
            opacity: 0;
            transition: opacity 0.3s ease;
             .project-link {
              display: flex;
              align-items: center;
              justify-content: center;
              width: 50px;
              height: 50px;
              background-color: white;
              border-radius: 50%;
              color: var(--primary-color);
              font-size: 1.2rem;
              text-decoration: none;
              transition: all 0.3s ease;
                 &:hover {
                  background-color: var(--dark-color);
                  color: white;
                }
            }
          }
        };
         .project-info {
          padding: 20px;
           h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: var(--dark-color);
          }
           p {
            color: var(--gray-color);
            margin-bottom: 15px;
          }
           .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
              span {
              background-color: #e9ecef;
              color: var(--dark-color);
              padding: 5px 10px;
              border-radius: 20px;
              font-size: 0.8rem;
              font-weight: 500;
            }
          }
        };
      };
     }
  }
   
  @media (max-width: 768px) {
    .projects-grid {
      grid-template-columns: 1fr;
    }
  }
  </style>