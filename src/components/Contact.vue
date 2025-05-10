<template>
    <section id="contact" class="contact">
      <div class="container">
        <h2 class="section-title">Contactez-moi</h2>
        <div class="contact-container">
          <div class="contact-info">
            <h3>Parlons de votre projet</h3>
            <p>Je suis disponible pour des opportunités de freelance ou d'emploi. N'hésitez pas à me contacter pour discuter de votre projet.</p>
            <div class="info-item">
              <i class="fas fa-envelope"></i>
              <span>princedossou465@gmail.com</span>
            </div>
            <div class="info-item">
              <i class="fas fa-phone"></i>
              <span>+229 01 51 87 92 55</span>
            </div>
            <div class="info-item">
              <i class="fas fa-map-marker-alt"></i>
              <span>Abomey-Calavi, Bénin</span>
            </div>
            <div class="social-links">
              <a href="#" target="_blank"><i class="fab fa-github"></i></a>
              <a href="#" target="_blank"><i class="fab fa-linkedin"></i></a>
              <a href="#" target="_blank"><i class="fab fa-twitter"></i></a>
              <a href="#" target="_blank"><i class="fab fa-instagram"></i></a>
            </div>
          </div>
          <form class="contact-form" @submit.prevent="submitForm">
            <div class="form-group">
              <input type="text" placeholder="Votre nom" required>
            </div>
            <div class="form-group">
              <input type="email" placeholder="Votre email" required>
            </div>
            <div class="form-group">
              <input type="text" placeholder="Sujet">
            </div>
            <div class="form-group">
              <textarea placeholder="Votre message" rows="5" required></textarea>
            </div>
            <button type="submit" class="btn">Envoyer le message</button>
          </form>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'Contact',
    methods: {
      submitForm() {
        alert('Message envoyé avec succès!');
        
      }
    }
  }
  </script>
  
  <style scoped>
  .contact {
    background-color: white;
  }
  
  .contact-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 50px;
  }
  
  .contact-info h3 {
    font-size: 1.8rem;
    margin-bottom: 20px;
    color: var(--dark-color);
  }
  
  .contact-info p {
    color: var(--gray-color);
    margin-bottom: 30px;
  }
  
  .info-item {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
  }
  
  .info-item i {
    width: 40px;
    height: 40px;
    background-color: #f8f9fa;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--primary-color);
    margin-right: 15px;
    font-size: 1.1rem;
  }
  
  .info-item span {
    color: var(--dark-color);
    font-weight: 500;
  }
  
  .social-links {
    display: flex;
    gap: 15px;
    margin-top: 30px;
  }
  
  .social-links a {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    background-color: #f8f9fa;
    border-radius: 50%;
    color: var(--dark-color);
    font-size: 1.2rem;
    transition: all 0.3s ease;
  }
  
  .social-links a:hover {
    background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
    color: white;
    transform: translateY(-3px);
  }
  
  .contact-form .form-group {
    margin-bottom: 20px;
  }
  
  .contact-form input,
  .contact-form textarea {
    width: 100%;
    padding: 12px 15px;
    border: 1px solid #e9ecef;
    border-radius: 5px;
    font-family: 'Inter', sans-serif;
    font-size: 1rem;
    transition: border-color 0.3s ease;
  }
  
  .contact-form input:focus,
  .contact-form textarea:focus {
    outline: none;
    border-color: var(--primary-color);
  }
  
  .contact-form textarea {
    resize: vertical;
  }
  
  @media (max-width: 768px) {
    .contact-container {
      grid-template-columns: 1fr;
    }
  }
  </style>