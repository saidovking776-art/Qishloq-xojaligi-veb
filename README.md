<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saidov Agro | 1-amaliy loyihasi</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">

    <style>
        :root {
            --primary: #1b8e4e;
            --primary-dark: #08602e;
            --primary-light: #eaf7ee;
            --gold: #a3831a;
            --text-dark: #1e293b;
            --text-muted: #64748b;
            --bg-body: #f4f7f5;
            --card-bg: #ffffff;
            --border-color: #e2e8f0;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Plus Jakarta Sans', system-ui, sans-serif;
        }

        body {
            background-color: var(--bg-body);
            color: var(--text-dark);
            line-height: 1.6;
        }

        .page-container {
            width: 100%;
            max-width: 1320px; 
            margin: 0 auto;
            padding: 0 20px;
        }

        header.top-header {
            background: #ffffff;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
            border-bottom: 2px solid #e2e8f0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .header-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 12px 0;
            gap: 15px;
        }

        .brand-box {
            display: flex;
            align-items: center;
            gap: 16px;
            text-decoration: none;
        }

        .brand-logo-img {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--primary);
            box-shadow: 0 4px 12px rgba(27, 142, 78, 0.2);
            transition: transform 0.3s ease;
            background-color: #fff;
        }

        .brand-logo-img:hover {
            transform: scale(1.08) rotate(3deg);
        }

        .brand-text h1 {
            font-size: 22px;
            font-weight: 800;
            color: var(--primary-dark);
            letter-spacing: 0.5px;
            line-height: 1.2;
        }

        .brand-text span {
            font-size: 13px;
            font-weight: 700;
            color: #b38719;
            text-transform: uppercase;
            letter-spacing: 1.2px;
            display: block;
        }

        .header-badge {
            background: var(--primary-light);
            color: var(--primary-dark);
            padding: 8px 16px;
            border-radius: 30px;
            font-size: 14px;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            border: 1px solid #c7ecd2;
        }

        .hero-banner {
            background: linear-gradient(135deg, #165b33 0%, #1b8e4e 100%);
            color: #ffffff;
            border-radius: 16px;
            padding: 40px 30px;
            margin: 30px 0;
            box-shadow: 0 10px 25px rgba(27, 142, 78, 0.15);
        }

        .hero-banner h2 {
            font-size: 26px;
            font-weight: 700;
            margin-bottom: 12px;
            line-height: 1.4;
        }

        .hero-banner p {
            font-size: 16px;
            color: #e2f4e8;
            max-width: 900px;
        }

        .cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }

        .agro-card {
            background: var(--card-bg);
            border-radius: 14px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.04);
            border: 1px solid var(--border-color);
            display: flex;
            flex-direction: column;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .agro-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.08);
        }

        .card-img-wrap {
            width: 100%;
            height: 240px;
            overflow: hidden;
            background: #e2e8f0;
            position: relative;
        }

        .card-img-wrap img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
            transition: transform 0.4s ease;
        }

        .agro-card:hover .card-img-wrap img {
            transform: scale(1.05);
        }

        .card-body {
            padding: 24px;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }

        .badge-tag {
            align-self: flex-start;
            background-color: var(--primary-light);
            color: var(--primary-dark);
            padding: 5px 12px;
            border-radius: 6px;
            font-size: 13px;
            font-weight: 700;
            margin-bottom: 14px;
            display: inline-flex;
            align-items: center;
            gap: 6px;
        }

        .card-body h3 {
            font-size: 18px;
            font-weight: 700;
            color: #1a331e;
            margin-bottom: 10px;
        }

        .card-body p {
            color: var(--text-muted);
            font-size: 15px;
            line-height: 1.6;
            text-align: justify;
        }

        .video-section {
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 14px;
            padding: 24px;
            margin-bottom: 50px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.04);
            text-align: center;
        }

        .video-wrapper {
            max-width: 800px;
            margin: 0 auto;
        }

        .video-wrapper video {
            width: 100%;
            height: auto;
            max-height: 500px;
            aspect-ratio: 16 / 9;
            object-fit: contain;
            border-radius: 10px;
            background-color: #000;
            display: block;
        }

        .video-caption {
            margin-top: 15px;
            font-size: 16px;
            font-weight: 600;
            color: var(--text-dark);
        }

        footer {
            background: #ffffff;
            border-top: 1px solid var(--border-color);
            padding: 25px 0;
            text-align: center;
            color: var(--text-muted);
            font-size: 14px;
            margin-top: 40px;
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                align-items: flex-start;
            }
            .header-badge {
                align-self: stretch;
                justify-content: center;
            }
            .hero-banner {
                padding: 25px 20px;
            }
            .hero-banner h2 {
                font-size: 20px;
            }
            .cards-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <header class="top-header">
        <div class="page-container header-content">
            <div class="brand-box">
                <img src="1313.jpg" alt="Saidov Agro" class="brand-logo-img">
                <div class="brand-text">
                    <h1>SAIDOV</h1>
                    <span>Agro Veb Xizmat</span>
                </div>
            </div>
            <div class="header-badge">
                <i class="fa-solid fa-award"></i> 1-chi Amaliy ish loyihasi
            </div>
        </div>
    </header>

    <div class="page-container">

        <section class="hero-banner">
            <h2>Qishloq xo‘jaligi — barqaror kelajak va oziq-ovqat xavfsizligi garovidir</h2>
            <p>
                O‘zbekiston zaminida dehqonchilik va bog‘dorchilik qadimdan shakllangan boy tajribaga ega. Quyoshli iqlim, zamonaviy agrotexnologiyalar va tomchilatib sug‘orish usullari orqali yuqori hosildorlik ta'minlanmoqda.
            </p>
        </section>

        <main class="cards-grid">

            <article class="agro-card">
                <div class="card-img-wrap">
                    <img src="1212.jpg" onerror="this.src='https://images.unsplash.com/photo-1500937386664-56d1dfef3854?w=800&auto=format&fit=crop&q=80'" alt="Ekin maydoni">
                </div>
                <div class="card-body">
                    <span class="badge-tag">
                        <i class="fa-solid fa-seedling"></i> 1-chi rasm
                    </span>
                    <h3>Ekin maydonlari va tabiat uyg‘unligi</h3>
                    <p>
                        Quyoshli iqlim va unumdor tuproq sababli yetishtirilgan meva-sabzavotlar o‘zining tabiiy shirinligi va foydali vitaminlari bilan mashhurdir.
                    </p>
                </div>
            </article>

            <article class="agro-card">
                <div class="card-img-wrap">
                    <img src="1213.jpg" onerror="this.src='https://images.unsplash.com/photo-1592982537447-7440770cbfc9?w=800&auto=format&fit=crop&q=80'" alt="Zamonaviy agrotexnika">
                </div>
                <div class="card-body">
                    <span class="badge-tag">
                        <i class="fa-solid fa-tractor"></i> 2-chi rasm
                    </span>
                    <h3>Zamonaviy texnikalar va unumdorlik</h3>
                    <p>
                        Zamonaviy traktorlar va agrotexnikalar dehqonlar mehnatini sezilarli yengillashtirib, ish samaradorligini oshiradi hamda qimmatli resurslarni tejaydi.
                    </p>
                </div>
            </article>

            <article class="agro-card">
                <div class="card-img-wrap">
                    <img src="1215.jpg" onerror="this.src='https://images.unsplash.com/photo-1563514227147-6d2ff665a6a0?w=800&auto=format&fit=crop&q=80'" alt="Tomchilatib sug‘orish tizimi">
                </div>
                <div class="card-body">
                    <span class="badge-tag">
                        <i class="fa-solid fa-droplet"></i> 3-chi rasm
                    </span>
                    <h3>Innovatsion tejamkor sug‘orish tizimlari</h3>
                    <p>
                        Tomchilatib sug‘orish texnologiyalari yordamida suv resurslari 40% gacha tejaladi va har bir niholga kerakli ozuqa aniq yetkazib beriladi.
                    </p>
                </div>
            </article>

        </main>

        <!-- Video bo'limi -->
        <section class="video-section">
            <div class="video-wrapper">
                <video controls preload="auto" playsinline>
                    <source src="1616.mp4">
                    Brauzeringiz ushbu videoni qo‘llab-quvvatlamaydi.
                </video>
            </div>
            <p class="video-caption">
                <i class="fa-solid fa-circle-play" style="color: var(--primary);"></i> Yerga ishlov berish jarayoni.
            </p>
        </section>

    </div>

    <footer>
        <div class="page-container">
            &copy; 2026 <strong>SAIDOV AGRO VEB XIZMAT</strong>. Barcha huquqlar himoyalangan.
        </div>
    </footer>

</body>
</html>
