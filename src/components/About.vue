<template>
    <section id="about" class="about">
      <div class="container">
        <h2 class="section-title">À propos de moi</h2>
        <div class="about-content">
          <div class="about-image">
            <img src="../assets/images/User.png" alt="Photo de profil">
          </div>
          <div class="about-text">
            <h3>Qui suis-je ?</h3>
            <p>Je suis un développeur passionné avec une expertise en développement web full stack. J'aime créer des applications web modernes, performantes et accessibles.</p>
            <p>Avec plusieurs années d'expérience, j'ai travaillé sur divers projets allant de simples sites vitrines à des applications web complexes. Je m'efforce toujours d'apprendre de nouvelles technologies et d'améliorer mes compétences.</p>
            <div class="about-info">
              <div class="info-item">
                <span>Nom :</span>
                <p>DOSSOU Prince</p>
              </div>
              <div class="info-item">
                <span>Email:</span>
                <p>princedossou465@gmail.com</p>
              </div>
              <div class="info-item">
                <span>Expérience:</span>
                <p>2 ans</p>
              </div>
              <div class="info-item">
                <span>Localisation:</span>
                <p>Abomey-Calavi, Bénin</p>
              </div>
            </div>
            <a href="#" class="btn">Télécharger mon CV</a>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'About'
  }
  </script>
  
  <style scoped>
  .about {
    background-color: #f8f9fa;
  }
  
  .about-content {
    display: flex;
    align-items: center;
    gap: 50px;
  }
  
  .about-image {
    flex: 1;
  }
  
  .about-image img {
    width: 100%;
    border-radius: 10px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
    animation: float 3s ease-in-out infinite;
  }
  
  .about-text {
    flex: 1;
  }
  
  .about-text h3 {
    font-size: 2rem;
    margin-bottom: 20px;
    color: var(--dark-color);
  }
  
  .about-text p {
    margin-bottom: 15px;
    color: var(--gray-color);
  }
  
  .about-info {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 10px;
    margin: 20px 0;
  }
  
  .info-item {
    display: flex;
    padding: 1rem;
  }
  
  .info-item span {
    display: flex;
    font-weight: 500;
    margin-right: 6px;
    color: var(--dark-color);
  }
  
  .info-item p {
    margin: 0;
    color: var(--gray-color);
  }
  @keyframes float {
    0% {
      transform: translateY(0);
    }
    50% {
      transform: translateY(-15px);
    }
    100% {
      transform: translateY(0);
    }
  }
  @media (max-width: 768px) {
    .about-content {
      flex-direction: column;
    }
  
    .about-info {
      grid-template-columns: 1fr;
    }
  }
  </style>