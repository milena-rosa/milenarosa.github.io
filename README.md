<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Boselli Dev - Tecnologia, Inovação e Desenvolvimento Mútuo</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #333;
            background: #fff;
        }

        /* Header e navegação */
        header {
            background: #2C2F48;
            padding: 1.5rem 2rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: #fff;
            text-decoration: none;
        }

        nav a {
            color: #fff;
            text-decoration: none;
            margin-left: 2rem;
            font-size: 0.95rem;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #4A9FBE;
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #2C2F48 0%, #1a1d2e 100%);
            color: #fff;
            padding: 6rem 2rem;
            text-align: center;
            /* min-height: 70vh; */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            font-weight: 700;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            color: #d0d0d0;
            max-width: 600px;
        }

        .cta-button {
            display: inline-block;
            background: #4A9FBE;
            color: #fff;
            padding: 1rem 2.5rem;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            transition: background 0.3s, transform 0.3s;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .cta-button:hover {
            background: #3a7fa0;
            transform: translateY(-2px);
        }

        /* Seções gerais */
        section {
            padding: 5rem 2rem;
        }

        section h2 {
            font-size: 2.2rem;
            margin-bottom: 3rem;
            color: #2C2F48;
            text-align: center;
        }

        section p {
            color: #555;
            line-height: 1.8;
        }

        /* Nossa Visão */
        .visao {
            background: #f9f9f9;
        }

        .visao-content {
            max-width: 700px;
            margin: 0 auto;
            text-align: center;
            font-size: 1.1rem;
        }

        .visao-content p {
            margin-bottom: 1.5rem;
        }

        /* Como Acreditamos - Grid de cards */
        .valores-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            max-width: 1100px;
            margin: 0 auto;
        }

        .valor-card {
            background: #f5f5f5;
            padding: 2rem;
            border-radius: 6px;
            border-left: 4px solid #4A9FBE;
            transition: box-shadow 0.3s, transform 0.3s;
        }

        .valor-card:hover {
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
            transform: translateY(-4px);
        }

        .valor-card h3 {
            color: #2C2F48;
            margin-bottom: 0.8rem;
            font-size: 1.1rem;
        }

        .valor-card p {
            font-size: 0.95rem;
            color: #666;
        }

        /* Quem Somos */
        .quem-somos {
            background: #fff;
        }

        .quem-somos-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .quem-somos-content p {
            margin-bottom: 1.5rem;
            font-size: 1.05rem;
        }

        .github-link {
            display: inline-block;
            margin-top: 1rem;
            color: #4A9FBE;
            text-decoration: none;
            font-weight: 600;
        }

        .github-link:hover {
            text-decoration: underline;
        }

        /* Contato */
        .contato {
            background: #2C2F48;
            color: #fff;
            text-align: center;
        }

        .contato h2 {
            color: #fff;
        }

        .contato-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 3rem;
            flex-wrap: wrap;
        }

        .contato-link {
            display: inline-flex;
            flex-direction: column;
            align-items: center;
            text-decoration: none;
            color: #fff;
            transition: opacity 0.3s;
        }

        .contato-link:hover {
            opacity: 0.8;
        }

        .contato-link-label {
            font-size: 0.9rem;
            color: #d0d0d0;
            margin-top: 0.5rem;
        }

        .contato-link-value {
            font-size: 1.05rem;
            font-weight: 600;
        }

        /* Footer */
        footer {
            background: #1a1d2e;
            color: #999;
            text-align: center;
            padding: 2rem;
            font-size: 0.9rem;
        }

        /* Responsivo */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            nav {
                display: none;
            }

            section {
                padding: 3rem 1rem;
            }

            section h2 {
                font-size: 1.8rem;
            }

            .valores-grid {
                grid-template-columns: 1fr;
            }

            .contato-links {
                gap: 1.5rem;
            }
        }

        /* Smooth scroll */
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-content">
            <a href="#" class="logo"><img src="https://assets.zyrosite.com/cdn-cgi/image/format=auto,w=100,fit=crop,q=95/mv0JEeDJkKh0pjX5/final-Rli9Q9TqZiPaXcbt.png" alt="Boselli Dev Logo" /></a>
            <nav>
                <a href="/#visao">Visão</a>
                <a href="/#valores">Como Acreditamos</a>
                <a href="/#quem">Quem Somos</a>
                <a href="/#contato">Contato</a>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <h1>Boselli Dev</h1>
        <p>Tecnologia, inovação e desenvolvimento mútuo</p>
        <p style="color: #bbb; font-size: 1rem; margin-top: 1rem;">Um espaço livre para criatividade, diversidade e autenticidade</p>
        <a href="/#contato" class="cta-button">Vamos conversar?</a>
    </section>

    <!-- Nossa Visão -->
    <section class="visao" id="visao">
        <div class="container">
            <h2>Nossa Visão</h2>
            <div class="visao-content">
                <p>
                    A Boselli Dev existe como um espaço de tecnologia e inovação. Um lugar onde criatividade, diversidade e autenticidade não são apenas bem-vindas — são essenciais.
                </p>
                <p>
                    Acreditamos que trabalho deve servir para algo além de gerar lucro. Que conhecimento deve ser compartilhado. Que todos crescem juntos. Ninguém fica pra trás.
                </p>
                <p>
                    Esse é o tipo de ambiente que queremos construir. Esse é o tipo de ambiente que acreditamos que deveria existir.
                </p>
            </div>
        </div>
    </section>

    <!-- Como Acreditamos -->
    <section id="valores">
        <div class="container">
            <h2>Como Acreditamos que Deveria Ser</h2>
            <div class="valores-grid">
                <div class="valor-card">
                    <h3>Propósito</h3>
                    <p>Trabalho que serve algo para além de gerar lucro.</p>
                </div>
                <div class="valor-card">
                    <h3>Time Fora da Curva</h3>
                    <p>Que questione porque as coisas são como são. Não só façam "porque é assim".</p>
                </div>
                <div class="valor-card">
                    <h3>Estímulo Intelectual</h3>
                    <p>Gente fina e elegante por perto. Diversidade de pensamento e experiência.</p>
                </div>
                <div class="valor-card">
                    <h3>Valorização</h3>
                    <p>Reconhecimento e remuneração proporcionais à qualidade das entregas. Entendedores entenderão.</p>
                </div>
                <div class="valor-card">
                    <h3>Comunicação Direta</h3>
                    <p>Assertiva, sem entrelinhas. Sem microgerenciamento. Sem feedbacks vagos e discriminatórios.</p>
                </div>
                <div class="valor-card">
                    <h3>Autonomia</h3>
                    <p>Dê o problema e o prazo. Confia na gente. Autonomia com confiança.</p>
                </div>
                <div class="valor-card">
                    <h3>Erro Construtivo</h3>
                    <p>Erros viram aprendizado e oportunidade. Sem busca por culpados. Já falei "sem microgerenciamento"?</p>
                </div>
                <div class="valor-card">
                    <h3>Aprendizado Ativo</h3>
                    <p>Oportunidade de aprender fazendo. Aplicar novos conhecimentos na prática e criar projetos para obter conhecimentos.</p>
                </div>
                <div class="valor-card">
                    <h3>Crescimento</h3>
                    <p>Como, quando e se você quiser. Sem julgamentos. Desenvolvimento mútuo.</p>
                </div>
                <div class="valor-card">
                    <h3>Liderança Genuína</h3>
                    <p>Gestor protege, impulsiona e corrige percursos.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Quem Somos -->
    <section class="quem-somos" id="quem">
        <div class="container">
            <h2>Quem Somos</h2>
            <div class="quem-somos-content">
                <p>
                    A Boselli Dev foi criada como um espaço onde é possível trabalhar de forma diferente. Um lugar onde pessoas neurodivergentes, superdotadas, criativas e simplesmente hartas de fingir que não veem as coisas absurdas possam prosperar.
                </p>
                <p>
                    Começamos com uma visão: o que deveria ser um lugar de trabalho realmente receptivo? O que deveria ser uma liderança genuína? Como deveria ser o tratamento com pessoas diferentes?
                </p>
                <p>
                    Essas perguntas nos guiam. E continuarão guiando tudo o que fazemos.
                </p>
                <p>
                    Conheça mais sobre o trabalho e ideias em meu
                    <a href="https://github.com/milena-rosa" target="_blank" class="github-link">portfolio no GitHub</a>.
                </p>
            </div>
        </div>
    </section>

    <!-- Contato -->
    <section class="contato" id="contato">
        <div class="container">
            <h2>Vamos Conversar?</h2>
            <div class="contato-links">
                <a href="https://github.com/milena-rosa" target="_blank" class="contato-link">
                    <div class="contato-link-value">GitHub</div>
                    <div class="contato-link-label">milena-rosa</div>
                </a>
                <a href="https://www.linkedin.com/in/milena-rosa/" target="_blank" class="contato-link">
                    <div class="contato-link-value">LinkedIn</div>
                    <div class="contato-link-label">milena-rosa</div>
                </a>
                <a href="mailto:milena@boselli.dev" class="contato-link">
                    <div class="contato-link-value">Email</div>
                    <div class="contato-link-label">milena@boselli.dev</div>
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 Boselli Dev. Tecnologia, inovação e desenvolvimento mútuo.</p>
    </footer>
</body>
</html>
