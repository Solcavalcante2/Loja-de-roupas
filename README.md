<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Loja de Roupas Femininas Elegante</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap');

  :root {
    --color-bg: #ffffff;
    --color-text-primary: #111827;
    --color-text-secondary: #6b7280;
    --color-accent: #000000;
    --color-accent-light: #333333;
    --border-radius: 0.75rem;
    --shadow-light: 0 4px 12px rgba(0,0,0,0.06);
    --transition-speed: 0.35s;
  }

  *, *::before, *::after {
    box-sizing: border-box;
  }
  body {
    margin: 0;
    font-family: 'Poppins', sans-serif;
    background-color: var(--color-bg);
    color: var(--color-text-secondary);
    line-height: 1.6;
    min-height: 100vh;
    scroll-behavior: smooth;
  }
  a {
    color: var(--color-accent);
    text-decoration: none;
    transition: color var(--transition-speed);
  }
  a:hover,
  a:focus {
    color: var(--color-accent-light);
    outline: none;
  }

  /* Container */
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1.25rem;
  }

  /* Navigation */
  header {
    position: sticky;
    top: 0;
    background: var(--color-bg);
    border-bottom: 1px solid #e5e7eb;
    z-index: 100;
    box-shadow: var(--shadow-light);
    transition: box-shadow var(--transition-speed);
  }
  header.scrolled {
    box-shadow: 0 8px 24px rgba(0,0,0,0.1);
  }
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    padding: 1rem 1.25rem;
  }
  .logo {
    font-size: 1.75rem;
    font-weight: 800;
    color: var(--color-text-primary);
    user-select: none;
    letter-spacing: 0.08em;
    transition: transform var(--transition-speed);
  }
  .logo:hover {
    transform: scale(1.05);
  }
  .nav-links {
    list-style: none;
    display: flex;
    gap: 2rem;
  }
  .nav-links li a {
    font-weight: 600;
    font-size: 1.125rem;
    color: var(--color-text-secondary);
    padding: 0.4rem 0.6rem;
    border-radius: 0.5rem;
    transition: background-color var(--transition-speed), color var(--transition-speed), transform 0.2s ease;
  }
  .nav-links li a:hover,
  .nav-links li a:focus {
    color: var(--color-accent);
    background-color: #f3f4f6;
    transform: scale(1.05);
    outline: none;
  }

  /* Hero Section */
  .hero {
    text-align: center;
    padding: 8rem 1.25rem 5rem;
    max-width: 850px;
    margin: 0 auto;
  }
  .hero h1 {
    font-size: 4rem;
    font-weight: 800;
    color: var(--color-text-primary);
    margin-bottom: 1rem;
    letter-spacing: -0.04em;
    line-height: 1.1;
    user-select: none;
    animation: fadeInUp 1s ease forwards;
    opacity: 0;
  }
  .hero p {
    font-size: 1.375rem;
    color: var(--color-text-secondary);
    margin-bottom: 2.5rem;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
    animation: fadeInUp 1s ease 0.3s forwards;
    opacity: 0;
  }
  .btn-primary {
    background-color: var(--color-accent);
    color: white;
    border: none;
    border-radius: var(--border-radius);
    padding: 1.25rem 3rem;
    font-size: 1.3rem;
    font-weight: 800;
    cursor: pointer;
    user-select: none;
    transition: background-color var(--transition-speed), box-shadow var(--transition-speed), transform 0.2s ease;
    box-shadow: 0 12px 32px rgba(0, 0, 0, 0.12);
    animation: fadeInUp 1s ease 0.6s forwards;
    opacity: 0;
    display: inline-block;
  }
  .btn-primary:hover,
  .btn-primary:focus {
    background-color: var(--color-accent-light);
    outline: none;
    box-shadow: 0 20px 48px rgba(0, 0, 0, 0.18);
    transform: scale(1.05);
  }

  /* Featured Products Section */
  .section {
    padding: 5rem 1.25rem 6rem;
    max-width: 1200px;
    margin: 0 auto;
  }
  .section h2 {
    font-size: 3rem;
    font-weight: 800;
    color: var(--color-text-primary);
    text-align: center;
    margin-bottom: 3.5rem;
    user-select: none;
    letter-spacing: -0.02em;
    animation: fadeInUp 1s ease forwards;
    opacity: 0;
  }

  /* Animate heading delay in products */
  #products h2 { animation-delay: 0s; }

  .products-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill,minmax(280px,1fr));
    gap: 3rem;
  }

  .product-card {
    background: var(--color-bg);
    border-radius: var(--border-radius);
    box-shadow: var(--shadow-light);
    overflow: hidden;
    display: flex;
    flex-direction: column;
    cursor: pointer;
    transition: transform var(--transition-speed), box-shadow var(--transition-speed);
    opacity: 0;
    animation: fadeInScale 0.7s ease forwards;
  }
  .product-card:nth-child(1) { animation-delay: 0.2s; }
  .product-card:nth-child(2) { animation-delay: 0.4s; }
  .product-card:nth-child(3) { animation-delay: 0.6s; }
  .product-card:nth-child(4) { animation-delay: 0.8s; }

  .product-card:hover,
  .product-card:focus-within {
    transform: translateY(-8px);
    box-shadow: 0 18px 32px rgba(0,0,0,0.15);
    outline: none;
  }
  .product-card img {
    width: 100%;
    height: auto;
    object-fit: cover;
    aspect-ratio: 4/5;
    transition: transform 0.4s ease;
  }
  .product-card:hover img,
  .product-card:focus-within img {
    transform: scale(1.05);
  }
  .product-info {
    padding: 1.25rem 1.75rem 2rem;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .product-name {
    font-weight: 700;
    font-size: 1.25rem;
    color: var(--color-text-primary);
    margin-bottom: 1rem;
    user-select: none;
    letter-spacing: 0.01em;
  }
  .product-price {
    font-weight: 700;
    color: var(--color-accent);
    font-size: 1.15rem;
    user-select: none;
  }

  /* About Section */
  .about {
    max-width: 900px;
    margin: 0 auto;
    padding: 0 1.25rem 5rem;
    text-align: center;
    animation: fadeInUp 1s ease 1.1s forwards;
    opacity: 0;
  }
  .about h2 {
    font-size: 3rem;
    font-weight: 800;
    margin-bottom: 1rem;
    color: var(--color-text-primary);
    user-select: none;
    letter-spacing: -0.01em;
  }
  .about p {
    font-size: 1.3125rem;
    max-width: 650px;
    margin-left: auto;
    margin-right: auto;
    color: var(--color-text-secondary);
    line-height: 1.7;
    user-select: text;
  }

  /* Newsletter Section */
  .newsletter {
    background: var(--color-bg);
    border-radius: var(--border-radius);
    box-shadow: var(--shadow-light);
    max-width: 600px;
    margin: 0 auto 7rem;
    padding: 3rem 2.5rem;
    text-align: center;
    animation: fadeInUp 1s ease 1.4s forwards;
    opacity: 0;
  }
  .newsletter h3 {
    font-weight: 800;
    font-size: 2.25rem;
    color: var(--color-text-primary);
    margin-bottom: 1.3rem;
    user-select: none;
    letter-spacing: -0.02em;
  }
  .newsletter p {
    color: var(--color-text-secondary);
    margin-bottom: 1.75rem;
    font-size: 1.125rem;
  }
  form {
    display: flex;
    max-width: 480px;
    margin-left: auto;
    margin-right: auto;
    gap: 1rem;
  }
  input[type="email"] {
    flex: 1;
    padding: 0.85rem 1.25rem;
    font-size: 1.15rem;
    border: 1.8px solid #d1d5db;
    border-radius: 0.5rem;
    outline-offset: 3px;
    transition: border-color var(--transition-speed), box-shadow var(--transition-speed);
    font-family: 'Poppins', sans-serif;
  }
  input[type="email"]::placeholder {
    color: var(--color-text-secondary);
  }
  input[type="email"]:focus {
    border-color: var(--color-accent);
    box-shadow: 0 0 8px var(--color-accent);
    outline: none;
  }
  button[type="submit"] {
    background-color: var(--color-accent);
    border: none;
    color: white;
    font-weight: 800;
    font-size: 1.25rem;
    padding: 0 2.5rem;
    border-radius: 0.5rem;
    cursor: pointer;
    user-select: none;
    transition: background-color var(--transition-speed), box-shadow var(--transition-speed), transform 0.15s ease;
    box-shadow: 0 12px 32px rgba(0, 0, 0, 0.16);
  }
  button[type="submit"]:hover,
  button[type="submit"]:focus {
    background-color: var(--color-accent-light);
    outline: none;
    box-shadow: 0 16px 40px rgba(59, 130, 246, 0.5);
    transform: scale(1.05);
  }
  button[type="submit"]:active {
    transform: scale(0.97);
  }

  /* Footer */
  footer {
    background: #f9fafb;
    text-align: center;
    padding: 2.75rem 1rem;
    font-size: 1rem;
    color: var(--color-text-secondary);
    user-select: none;
    letter-spacing: 0.02em;
  }

  /* Utility for screen reader only text */
  .sr-only {
    position: absolute !important;
    width: 1px !important;
    height: 1px !important;
    padding: 0 !important;
    margin: -1px !important;
    overflow: hidden !important;
    clip: rect(0,0,0,0) !important;
    border: 0 !important;
  }

  /* Animations */
  @keyframes fadeInUp {
    0% {
      opacity: 0;
      transform: translateY(25px);
    }
    100% {
      opacity: 1;
      transform: translateY(0);
    }
  }
  @keyframes fadeInScale {
    0% {
      opacity: 0;
      transform: scale(0.9);
    }
    100% {
      opacity: 1;
      transform: scale(1);
    }
  }

  /* Responsive */
  @media (max-width: 600px) {
    .hero h1 {
      font-size: 2.75rem;
    }
    .hero p {
      font-size: 1.125rem;
    }
    .btn-primary {
      font-size: 1.1rem;
      padding: 1rem 2rem;
      box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
    }
    .products-grid {
      grid-template-columns: repeat(auto-fill,minmax(220px,1fr));
      gap: 2rem;
    }
    .product-name {
      font-size: 1.1rem;
    }
    .product-price {
      font-size: 1.05rem;
    }
    form {
      flex-direction: column;
    }
    button[type="submit"] {
      width: 100%;
      padding: 0.9rem 0;
      font-size: 1.15rem;
    }
  }

</style>
</head>
<body>
  <header>
    <nav role="navigation" aria-label="Menu principal" class="container">
      <div class="logo" tabindex="0">Feminina</div>
      <ul class="nav-links">
        <li><a href="#products" tabindex="0">Produtos</a></li>
        <li><a href="#about" tabindex="0">Sobre</a></li>
        <li><a href="#newsletter" tabindex="0">Newsletter</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="hero" role="banner" aria-label="Apresentação da loja">
      <h1>JR moda feminina</h1>
      <p>Descubra as últimas tendências para renovar seu guarda-roupa com peças exclusivas e cheias de personalidade.</p>
      <a href="#products" class="btn-primary" tabindex="0">Compre Agora</a>
    </section>

    <section id="products" class="section" aria-label="Produtos em destaque">
      <h2>Produtos em Destaque</h2>
      <div class="products-grid">
        <article class="product-card" tabindex="0" role="group" aria-label="Vestido Longo - R$160,00">
          <img src="https://images.unsplash.com/photo-1503342217505-b0a15ec3261c?auto=format&amp;fit=crop&amp;w=500&amp;q=80" alt="Vestido Longo com detalhes delicados" loading="lazy" />
          <div class="product-info">
            <h3 class="product-name">Vestido Longo</h3>
            <span class="product-price">R$ 160,00</span>
          </div>
        </article>
        <article class="product-card" tabindex="0" role="group" aria-label="Vestido Júlia - R$149,90">
          <img src="https://images.unsplash.com/photo-1542068829-1115f7259450?auto=format&amp;fit=crop&amp;w=500&amp;q=80" alt="Vestido Júlia elegante em tom pastel" loading="lazy" />
          <div class="product-info">
            <h3 class="product-name">Vestido Júlia</h3>
            <span class="product-price">R$ 149,90</span>
          </div>
        </article>
        <article class="product-card" tabindex="0" role="group" aria-label="Calça Pantalona - R$160,00">
          <img src="https://images.unsplash.com/photo-1495121605193-b116b5b09e8b?auto=format&amp;fit=crop&amp;w=500&amp;q=80" alt="Calça Pantalona preta com caimento fluido" loading="lazy" />
          <div class="product-info">
            <h3 class="product-name">Calça Pantalona</h3>
            <span class="product-price">R$ 160,00</span>
          </div>
        </article>
        <article class="product-card" tabindex="0" role="group" aria-label="Jaqueta Jeans - R$249,90">
          <img src="https://images.unsplash.com/photo-1534311220386-5f09d5dd9b97?auto=format&amp;fit=crop&amp;w=500&amp;q=80" alt="Jaqueta Jeans clássica azul" loading="lazy" />
          <div class="product-info">
            <h3 class="product-name">Jaqueta Jeans</h3>
            <span class="product-price">R$ 249,90</span>
          </div>
        </article>
      </div>
    </section>

    <section id="about" class="about" aria-label="Sobre a loja">
      <h2>Sobre a Feminina</h2>
      <p>Somos uma loja dedicada a oferecer moda feminina que une conforto, elegância e exclusividade. Cada peça é escolhida com cuidado para que você se sinta única em qualquer ocasião.</p>
    </section>

    <section id="newsletter" class="newsletter" aria-label="Assinar newsletter">
      <h3>Fique por dentro das novidades</h3>
      <p>Assine nossa newsletter e receba ofertas exclusivas e lançamentos em primeira mão.</p>
      <form id="newsletterForm" novalidate>
        <label for="emailInput" class="sr-only">Seu e-mail</label>
        <input type="email" id="emailInput" name="email" placeholder="Digite seu e-mail" required aria-required="true" />
        <button type="submit">Assinar</button>
      </form>
      <p id="newsletterMessage" role="alert" aria-live="polite" style="color: var(--color-accent); margin-top: 1rem; display:none;"></p>
    </section>
  </main>

  <footer>
    <div class="container" aria-label="Rodapé">
      © 2024 Feminina - Todos os direitos reservados.
    </div>
  </footer>

<script>
  (function(){
    const form = document.getElementById('newsletterForm');
    const emailInput = document.getElementById('emailInput');
    const message = document.getElementById('newsletterMessage');
    const header = document.querySelector('header');

    form.addEventListener('submit', function(e) {
      e.preventDefault();
      message.style.display = 'none';

      if (!emailInput.value.trim()) {
        message.textContent = 'Por favor, insira um e-mail válido.';
        message.style.color = '#dc2626'; // Red for error
        message.style.display = 'block';
        emailInput.focus();
        return;
      }

      const pattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      if (!pattern.test(emailInput.value.trim())) {
        message.textContent = 'Formato de e-mail inválido.';
        message.style.color = '#dc2626';
        message.style.display = 'block';
        emailInput.focus();
        return;
      }

      setTimeout(() => {
        message.textContent = 'Obrigado por assinar nossa newsletter!';
        message.style.color = 'var(--color-accent)';
        message.style.display = 'block';
        emailInput.value = '';
      }, 800);
    });

    // Header shadow animation on scroll
    window.addEventListener('scroll', () => {
      if(window.scrollY > 10){
        header.classList.add('scrolled');
      } else {
        header.classList.remove('scrolled');
      }
    });
  })();
</script>
</body>
</html>

