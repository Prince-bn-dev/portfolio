<template>
    <section class="hero">
      <div class="container">
        <div class="hero-content">
          <h1>Bonjour, je suis <span class="text-gradient">DOSSOU PRINCE</span></h1>
          <h2>Développeur Full Stack</h2>
          <p>Je crée des expériences web modernes et performantes avec une attention particulière aux détails.</p>
          <div class="hero-buttons">
            <a href="#contact" class="btn">Me contacter</a>
            <a href="#projects" class="btn btn-outline">Voir mes projets</a>
          </div>
        </div>
        <div class="hero-image">
          <img src="../assets/images/user.jpg" alt="Illustration du développeur">
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Hero'
  }
  </script>
  
  <style scoped lang="scss">
  .hero {
    padding: 150px 0 100px;
    background-color: var(--dark-color);


    .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    }
     .hero-content {
      max-width: 600px;
      h1 {
    font-size: 3.5rem;
    font-weight: 700;
    margin-bottom: 20px;
    line-height: 1.2;
    color: var(--light-color);
  }
  h2 {
    font-size: 1.8rem;
    font-weight: 400;
    color: var(--gray-color);
    margin-bottom: 20px;
  }
  p {
    font-size: 1.1rem;
    margin-bottom: 30px;
    color: var(--gray-color);
  }
  .hero-buttons {
    display: flex;
    gap: 20px;

    .btn-outline {
    background: transparent;
    border: 2px solid var(--primary-color);
    color: var(--primary-color);
    &:hover {
    background: var(--primary-color);
    color: white;
  }
  }
  }
    }
  }
  
  .hero-image img {
    max-width: 400px;
    height: 400px;
    border-radius: 100%;
    animation: float 3s ease-in-out infinite;
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
  
  @media (max-width: 992px) {
    .hero .container {
      flex-direction: column;
      text-align: center;
    }
  
    .hero-content {
      margin-bottom: 50px;
    }
  
    .hero-buttons {
      justify-content: center;
    }
  
    .hero-content h1 {
      font-size: 2.5rem;
    }
  
    .hero-content h2 {
      font-size: 1.5rem;
    }
  }
  </style>