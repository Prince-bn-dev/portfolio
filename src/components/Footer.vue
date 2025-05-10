<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-logo">
          <a href="#">DOSSOU<span>Prince</span></a>
          <p>Développeur Full Stack passionné par la création d'applications web modernes et performantes.</p>
        </div>
        <div class="footer-links">
          <h3>Liens rapides</h3>
          <ul>
            <li><a href="#about">À propos</a></li>
            <li><a href="#skills">Compétences</a></li>
            <li><a href="#projects">Projets</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </div>
        <div class="footer-contact">
          <h3>Contact</h3>
          <ul>
            <li><i class="fas fa-envelope"></i> princedossou465@gmail.com</li>
            <li><i class="fas fa-phone"></i> +229 01 51 87 92 55</li>
            <li><i class="fas fa-map-marker-alt"></i>Abomey-Calavi, Bénin</li>
          </ul>
        </div>
      </div>
      <div class="footer-bottom">
        <p>&copy; {{ currentYear }} dossouprince. Tous droits réservés.</p>
        <div class="footer-social">
          <a href="#" target="_blank"><i class="fab fa-github"></i></a>
          <a href="#" target="_blank"><i class="fab fa-linkedin"></i></a>
          <a href="#" target="_blank"><i class="fab fa-twitter"></i></a>
          <a href="#" target="_blank"><i class="fab fa-instagram"></i></a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      currentYear: new Date().getFullYear()
    }
  }
}
</script>

<style scoped>
.footer {
  background-color: var(--dark-color);
  color: white;
  padding: 80px 0 20px;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 50px;
  margin-bottom: 50px;
}

.footer-logo a {
  font-size: 1.8rem;
  font-weight: 700;
  text-decoration: none;
  color: white;
}

.footer-logo span {
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.footer-logo p {
  margin-top: 20px;
  color: rgba(255, 255, 255, 0.7);
}

.footer-links h3,
.footer-contact h3 {
  font-size: 1.5rem;
  margin-bottom: 20px;
  position: relative;
  padding-bottom: 10px;
}

.footer-links h3::after,
.footer-contact h3::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 50px;
  height: 3px;
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
}

.footer-links ul,
.footer-contact ul {
  list-style: none;
}

.footer-links li {
  margin-bottom: 10px;
}

.footer-links a {
  color: rgba(255, 255, 255, 0.7);
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-links a:hover {
  color: var(--primary-color);
}

.footer-contact li {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
  color: rgba(255, 255, 255, 0.7);
}

.footer-contact i {
  margin-right: 10px;
  color: var(--primary-color);
}

.footer-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 20px;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.footer-bottom p {
  color: rgba(255, 255, 255, 0.5);
  font-size: 0.9rem;
}

.footer-social {
  display: flex;
  gap: 15px;
}

.footer-social a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  background-color: rgba(255, 255, 255, 0.1);
  border-radius: 50%;
  color: white;
  font-size: 1.2rem;
  transition: all 0.3s ease;
}

.footer-social a:hover {
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  transform: translateY(-3px);
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
  }

  .footer-bottom {
    flex-direction: column;
    gap: 20px;
    text-align: center;
  }
}
</style>