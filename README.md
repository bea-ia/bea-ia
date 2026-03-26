<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Carta de Presentación</title>

  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

  <style>
    * { box-sizing: border-box; }

    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #4facfe, #00f2fe);
      color: #333;
    }

    main {
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 20px;
    }

    .container {
      max-width: 800px;
      width: 100%;
      background: white;
      border-radius: 15px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.15);
      overflow: hidden;
      animation: fadeInUp 1s ease;
    }

    /* HEADER */
    header {
      background: #007BFF;
      color: white;
      padding: 30px;
      text-align: center;
    }

    /* ✨ TYPEWRITER */
    .typewriter {
      overflow: hidden;
      white-space: nowrap;
      border-right: 3px solid white;
      width: 0;
      animation: typing 3s steps(30, end) forwards, blink 0.8s infinite;
    }

    .subtitle {
      opacity: 0;
      animation: fadeIn 2s ease forwards;
      animation-delay: 2.5s;
    }

    /* CONTENIDO */
    section {
      padding: 30px;
      opacity: 0;
      transform: translateY(40px);
      transition: all 0.8s ease;
    }

    section.show {
      opacity: 1;
      transform: translateY(0);
    }

    h2 {
      margin-top: 0;
      color: #444;
    }

    p {
      line-height: 1.6;
      margin: 15px 0;
    }

    .highlight {
      color: #007BFF;
      font-weight: 600;
    }

    /* HABILIDADES */
    .skills p {
      margin: 8px 0;
      transition: transform 0.3s ease, color 0.3s ease;
    }

    .skills p:hover {
      transform: translateX(10px);
      color: #007BFF;
    }

    /* BOTONES */
    .buttons {
      margin-top: 20px;
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }

    .btn {
      text-decoration: none;
      padding: 12px 20px;
      border-radius: 8px;
      font-weight: 500;
      transition: all 0.3s ease;
    }

    .github {
      background: #24292e;
      color: white;
    }

    .github:hover {
      background: #000;
      transform: translateY(-3px);
    }

    .email {
      background: #007BFF;
      color: white;
    }

    .email:hover {
      background: #0056b3;
      transform: translateY(-3px);
    }

    /* FOOTER */
    footer {
      text-align: center;
      padding: 20px;
      font-size: 14px;
      background: #f1f1f1;
    }

    /* ANIMACIONES */
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(40px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes typing {
      from { width: 0 }
      to { width: 100% }
    }

    @keyframes blink {
      50% { border-color: transparent }
    }

  </style>
</head>
<body>

  <main>
    <div class="container">

      <!-- HEADER -->
      <header>
        <h1 class="typewriter">Hola, soy Beatriz <Canvas></Canvas>👋</h1>
        <p class="subtitle">Ingeniera en IA en formación</p>
      </header>

      <!-- SOBRE MÍ -->
      <section>
        <h2>Sobre mí</h2>
        <p>
          Actualmente estoy formándome en <span class="highlight">Ingeniería de Inteligencia Artificial</span> en 4Geeks Academy.
        </p>
        <p>
          Tengo conocimientos en <span class="highlight">HTML, CSS y JavaScript</span>.
        </p>
        <p>
          Cuento con experiencia en <span class="highlight">trabajo en equipo</span> y me adapto fácilmente a nuevos retos.
        </p>
      </section>

      <!-- HABILIDADES -->
      <section>
        <h2>Habilidades</h2>
        <div class="skills">
          <p>✔ HTML</p>
          <p>✔ CSS</p>
          <p>✔ JavaScript</p>
          <p>✔ Trabajo en equipo</p>
        </div>
      </section>

      <!-- CONTACTO -->
      <section>
        <h2>Contacto</h2>
        <div class="buttons">
          <a href="https://github.com/bea-ia" target="_blank" class="btn github">
            Ver mi GitHub
          </a>

          <a href="mailto:beacid95@gmail.com" class="btn email">
            Contactar por Email
          </a>
        </div>
      </section>

      <!-- FOOTER -->
      <footer>
        <p>© 2026 - beatriz | Gracias por visitar mi perfil 🙌</p>
      </footer>

    </div>
  </main>

  <!-- JS SCROLL ANIMATION -->
  <script>
    const sections = document.querySelectorAll("section");

    const revealOnScroll = () => {
      const trigger = window.innerHeight * 0.85;

      sections.forEach(section => {
        const top = section.getBoundingClientRect().top;

        if (top < trigger) {
          section.classList.add("show");
        }
      });
    };

    window.addEventListener("scroll", revealOnScroll);
    revealOnScroll();
  </script>

</body>
</html>
