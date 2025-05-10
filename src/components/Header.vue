<template>
  <header class="header" @scroll="navScroll">
    <div class="container">
      <nav class="nav">
        <div class="logo">
          <a href="#">D.<span>P</span></a>
        </div>
        <ul class="nav-links">
          <li><a href="#about">À propos</a></li>
          <li><a href="#skills">Compétences</a></li>
          <li><a href="#projects">Projets</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
        <div class="hamburger" @click="toggleMenu">
          <div class="line top"></div>
          <div class="line center"></div>
          <div class="line bottom"></div>
        </div>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  methods: {
    toggleMenu() {
      const navLinks = document.querySelector('.nav-links');
      navLinks.classList.toggle('active');
    },
    navScroll(){
      if (window.scrollY>20 ) {
        const header = document.querySelector('.header');
        header.classList.add('.header-scroll')
      }

    }
    
  },
  mounted() {
    // Fermer le menu mobile quand on clique sur un lien
    const navLinks = document.querySelectorAll('.nav-links a');
    navLinks.forEach(link => {
      link.addEventListener('click', () => {
        const navLinks = document.querySelector('.nav-links');
        navLinks.classList.remove('active');
      });
    });
  }
}
</script>

<style scoped lang="scss">
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  background-color: var(--dark-color);
  color: var(--light-color);
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  padding: 20px 0;
}
.header-scroll {
  background-color: var(--secondary-color) !important;
  color: var(--dark-color);
}

.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo a {
  font-size: 1.8rem;
  font-weight: 700;
  text-decoration: none;
  color: var(--light-color);
}

.logo span {
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.nav-links {
  display: flex;
  list-style: none;
}

.nav-links li {
  margin-left: 30px;
}

.nav-links a {
  text-decoration: none;
  color: var(--light-color);
  font-weight: 500;
  font-size: 1.1rem;
  transition: color 0.3s ease;
  position: relative;
}

.nav-links a:hover {
  color: var(--primary-color);
}

.nav-links a::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
  transition: width 0.3s ease;
}

.nav-links a:hover::after {
  width: 100%;
}

.hamburger {
  display: none;
  cursor: pointer;
}

.hamburger .line {
  width: 25px;
  height: 3px;
  background-color: var(--light-color);
  margin: 5px;
  transition: all 0.3s ease;
}

@media (max-width: 768px) {
  .nav-links {
    position: fixed;
    top: 80px;
    left: -100%;
    width: 100%;
    height: calc(100vh - 80px);
    background-color: var(--dark-color);
    flex-direction: column;
    align-items: center;
    justify-content: center;
    transition: left 0.5s ease;
  }

  .nav-links.active {
    left: 0;
  }

  .nav-links li {
    margin: 20px 0;
  }

  .hamburger {
    display: block;
    &:hover{
      transition: all ease-in 9s;
      .center{
        display: none;
      }
      
    }
  }
}
</style>