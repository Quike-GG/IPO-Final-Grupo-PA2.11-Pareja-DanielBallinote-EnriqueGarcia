[index.html](https://github.com/user-attachments/files/25602895/index.html)HTML

[Upl<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kairos | Encuentra tu Momento Óptimo</title>
    <style>
        :root {
            --primary: #2A9D8F; /* Verde azulado calmante */
            --secondary: #264653; /* Azul oscuro profundo */
            --accent: #E9C46A; /* Amarillo suave para destacar */
            --light: #F4F9F9;
            --text: #333333;
            --white: #ffffff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
        }

        body {
            background-color: var(--light);
            color: var(--text);
            line-height: 1.6;
        }

        /* Header */
        header {
            background-color: var(--white);
            padding: 1rem 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--secondary);
            letter-spacing: 2px;
        }

        .logo span {
            color: var(--primary);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            text-decoration: none;
            color: var(--secondary);
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--primary);
        }

        .btn-cta {
            background-color: var(--primary);
            color: var(--white);
            padding: 0.7rem 1.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: transform 0.3s, background-color 0.3s;
        }

        .btn-cta:hover {
            background-color: var(--secondary);
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 5rem 10%;
            background: linear-gradient(135deg, var(--white) 0%, #e0f7fa 100%);
            min-height: 80vh;
        }

        .hero-text {
            flex: 1;
            padding-right: 2rem;
        }

        .hero h1 {
            font-size: 3.5rem;
            color: var(--secondary);
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.2rem;
            color: #555;
            margin-bottom: 2rem;
            max-width: 500px;
        }

        .hero-image {
            flex: 1;
            text-align: center;
        }

        .chip-visual {
            width: 300px;
            height: 300px;
            background: radial-gradient(circle, var(--primary) 0%, transparent 70%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto;
            position: relative;
            animation: pulse 3s infinite;
        }

        .chip-icon {
            font-size: 5rem;
            color: var(--white);
            z-index: 2;
        }

        @keyframes pulse {
            0% { transform: scale(1); opacity: 0.8; }
            50% { transform: scale(1.05); opacity: 1; }
            100% { transform: scale(1); opacity: 0.8; }
        }

        /* Features */
        .features {
            padding: 5rem 10%;
            background-color: var(--white);
        }

        .section-title {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 1rem;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
        }

        .feature-card {
            padding: 2rem;
            border-radius: 15px;
            background-color: var(--light);
            transition: transform 0.3s;
            border: 1px solid #eee;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
        }

        .feature-icon {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }

        .feature-card h3 {
            margin-bottom: 1rem;
            color: var(--secondary);
        }

        /* How it Works */
        .how-it-works {
            padding: 5rem 10%;
            background-color: var(--secondary);
            color: var(--white);
            text-align: center;
        }

        .steps {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin-top: 3rem;
            gap: 2rem;
        }

        .step {
            flex: 1;
            min-width: 250px;
        }

        .step-number {
            font-size: 4rem;
            font-weight: 700;
            color: rgba(255,255,255,0.1);
            line-height: 1;
            margin-bottom: -20px;
            display: block;
        }

        .step h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--accent);
        }

        /* Testimonials based on Needfinding */
        .testimonials {
            padding: 5rem 10%;
            background-color: var(--light);
        }

        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .testimonial-card {
            background: var(--white);
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            font-style: italic;
        }

        .testimonial-author {
            margin-top: 1.5rem;
            font-weight: 600;
            color: var(--secondary);
            font-style: normal;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .badge {
            background-color: var(--primary);
            color: white;
            padding: 2px 8px;
            border-radius: 4px;
            font-size: 0.8rem;
            font-style: normal;
        }

        /* Footer */
        footer {
            background-color: #1a1a1a;
            color: #888;
            padding: 3rem 10%;
            text-align: center;
        }

        footer p {
            margin-bottom: 1rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero {
                flex-direction: column;
                text-align: center;
                padding-top: 2rem;
            }
            
            .hero-text {
                padding-right: 0;
                margin-bottom: 3rem;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            nav ul {
                display: none; /* Simplificado para el ejemplo */
            }
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <div class="logo">KAIROS<span>.TECH</span></div>
        <nav>
            <ul>
                <li><a href="#features">Tecnología</a></li>
                <li><a href="#how">Cómo funciona</a></li>
                <li><a href="#testimonials">Historias</a></li>
            </ul>
        </nav>
        <a href="#preorder" class="btn-cta">Reservar Acceso</a>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-text">
            <h1>No necesitas más tiempo.<br>Necesitas el momento adecuado.</h1>
            <p>El primer implante neural biocompatible que sincroniza tu ritmo biológico con tu día a día. Detecta tu estrés, optimiza tu foco y protege tu salud mental antes de que llegue el burnout.</p>
            <a href="#preorder" class="btn-cta">Descubre Kairos</a>
        </div>
        <div class="hero-image">
            <div class="chip-visual">
                <div class="chip-icon">🧠</div>
            </div>
            <p style="margin-top: 1rem; font-size: 0.9rem; color: #666;">Tecnología de malla de grafeno invisible</p>
        </div>
    </section>

    <!-- Features -->
    <section id="features" class="features">
        <div class="section-title">
            <h2>Tu biología, optimizada</h2>
            <p>Kairos no es un wearable. Es parte de ti. Diseñado para escucharte cuando tú no puedes.</p>
        </div>
        <div class="features-grid">
            <div class="feature-card">
                <div class="feature-icon">⚗️</div>
                <h3>Sensado Químico</h3>
                <p>Monitoreo en tiempo real de cortisol, dopamina y marcadores de estrés directamente en el fluido intersticial. Sabemos cómo te sientes antes que tú.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">⏳</div>
                <h3>Gestión del Tiempo Biológico</h3>
                <p>La app te indica cuándo es el momento óptimo para tareas complejas y cuándo es vital descansar, basándose en tu energía real, no en el reloj.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">🛡️</div>
                <h3>Prevención de Salud</h3>
                <p>Detecta patrones de irregularidad mental continuada. Recibe alertas tempranas para prevenir ansiedad crónica o depresión antes de que se manifiesten.</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">🔒</div>
                <h3>Privacidad Total</h3>
                <p>Tus datos neuronales se procesan localmente. Tú eres el único dueño de tu mente. Encriptación de grado militar incluida.</p>
            </div>
        </div>
    </section>

    <!-- How it Works -->
    <section id="how" class="how-it-works">
        <div class="section-title">
            <h2 style="color: white;">Flujo Natural</h2>
        </div>
        <div class="steps">
            <div class="step">
                <span class="step-number">01</span>
                <h3>Implante Invisible</h3>
                <p>Procedimiento mínimamente invasivo. Malla flexible que se adapta a tu cerebro sin rechazo.</p>
            </div>
            <div class="step">
                <span class="step-number">02</span>
                <h3>Sincronización</h3>
                <p>Kairos aprende tus ciclos en 7 días. Conecta con tu móvil para organizar tu agenda automáticamente.</p>
            </div>
            <div class="step">
                <span class="step-number">03</span>
                <h3>Vida en Equilibrio</h3>
                <p>Trabaja cuando tu dopamina es alta. Descansa cuando tu cortisol sube. Sin vibraciones, solo guía.</p>
            </div>
        </div>
    </section>

    <!-- Testimonials (Based on Needfinding PDF) -->
    <section id="testimonials" class="testimonials">
        <div class="section-title">
            <h2>Lo que dicen los primeros usuarios</h2>
        </div>
        <div class="testimonial-grid">
            <div class="testimonial-card">
                <p>"El mayor problema en mi empresa es el burnout silencioso. Kairos detectó mis picos de estrés semanas antes de que yo colapsara. Me dijo cuándo parar y salvó mi salud mental."</p>
                <div class="testimonial-author">
                    Clara Vázquez <span class="badge">34 años, RRHH</span>
                </div>
            </div>
            <div class="testimonial-card">
                <p>"Como estudiante, nunca sabía cuándo estudiar. Kairos me avisa cuando mi cerebro está químicamente listo para concentrarse. Mis notas han mejorado sin estudiar más horas."</p>
                <div class="testimonial-author">
                    Guillermo C. <span class="badge">19 años, Estudiante</span>
                </div>
            </div>
            <div class="testimonial-card">
                <p>"Me preocupaba la privacidad, pero al ver que los datos no salen de mi dispositivo, me tranquilicé. Es como tener un asistente que conoce mi cuerpo mejor que yo."</p>
                <div class="testimonial-author">
                    Pedro Calvillo <span class="badge">69 años, Jubilado</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Kairos Neurotech. Todos los derechos reservados.</p>
        <p>Diseñado para el bienestar humano. Tecnología biocompatible.</p>
        <p style="font-size: 0.8rem; margin-top: 2rem;">Aviso: El implante Kairos requiere procedimiento médico certificado. Consulte a su especialista.</p>
    </footer>

</body>
</html>oading index.html…]()
