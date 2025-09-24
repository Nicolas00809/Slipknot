Site sobre a Banda Slipknot

Vou criar um site completo e responsivo sobre a banda Slipknot usando HTML e CSS. O site incluirá informações sobre a banda, discografia, membros e mais.

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Slipknot - A Nona Maravilha do Metal</title>
    <style>
        /* Reset e estilos gerais */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #0a0a0a;
            color: #f0f0f0;
            line-height: 1.6;
        }
        
        a {
            text-decoration: none;
            color: #c1121f;
            transition: color 0.3s;
        }
        
        a:hover {
            color: #ff2a3a;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Cabeçalho */
        header {
            background-color: #000;
            padding: 20px 0;
            border-bottom: 3px solid #c1121f;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .logo {
            text-align: center;
            margin-bottom: 15px;
        }
        
        .logo h1 {
            font-size: 2.5rem;
            color: #c1121f;
            text-shadow: 0 0 10px rgba(193, 18, 31, 0.7);
            letter-spacing: 2px;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            flex-wrap: wrap;
        }
        
        nav ul li {
            margin: 0 15px;
        }
        
        nav ul li a {
            font-weight: bold;
            font-size: 1.1rem;
            padding: 5px 10px;
            border-radius: 3px;
        }
        
        nav ul li a:hover {
            background-color: rgba(193, 18, 31, 0.2);
        }
        
        /* Banner */
        .banner {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), 
                        url('https://images.unsplash.com/photo-1516280440614-37939bbacd81?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            height: 70vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 20px;
        }
        
        .banner-content h2 {
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.8);
        }
        
        .banner-content p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: #c1121f;
            color: white;
            padding: 12px 25px;
            border-radius: 5px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s;
        }
        
        .btn:hover {
            background-color: #ff2a3a;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(193, 18, 31, 0.4);
        }
        
        /* Seções */
        section {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: #c1121f;
            display: inline-block;
            padding-bottom: 10px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            width: 100px;
            height: 3px;
            background-color: #c1121f;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
        
        /* Sobre */
        .about-content {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 30px;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
        }
        
        .about-image {
            flex: 1;
            min-width: 300px;
            text-align: center;
        }
        
        .about-image img {
            max-width: 100%;
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(193, 18, 31, 0.3);
        }
        
        /* Membros */
        .members-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .member-card {
            background-color: #1a1a1a;
            border-radius: 5px;
            overflow: hidden;
            transition: transform 0.3s;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.5);
        }
        
        .member-card:hover {
            transform: translateY(-10px);
        }
        
        .member-image {
            height: 250px;
            background-size: cover;
            background-position: center;
        }
        
        .member-info {
            padding: 20px;
        }
        
        .member-info h3 {
            color: #c1121f;
            margin-bottom: 10px;
        }
        
        /* Discografia */
        .discography {
            background-color: #111;
        }
        
        .albums-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 30px;
        }
        
        .album-card {
            background-color: #1a1a1a;
            border-radius: 5px;
            overflow: hidden;
            transition: transform 0.3s;
        }
        
        .album-card:hover {
            transform: scale(1.05);
        }
        
        .album-cover {
            height: 200px;
            background-size: cover;
            background-position: center;
        }
        
        .album-info {
            padding: 15px;
            text-align: center;
        }
        
        .album-info h3 {
            margin-bottom: 5px;
        }
        
        .album-info p {
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Tour */
        .tour-dates {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .tour-item {
            background-color: #1a1a1a;
            margin-bottom: 15px;
            border-radius: 5px;
            overflow: hidden;
            display: flex;
            flex-wrap: wrap;
        }
        
        .tour-date {
            background-color: #c1121f;
            padding: 15px;
            min-width: 120px;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .tour-info {
            padding: 15px;
            flex: 1;
        }
        
        .tour-info h3 {
            margin-bottom: 5px;
        }
        
        .tour-btn {
            background-color: #333;
            padding: 10px 15px;
            border-radius: 3px;
            font-size: 0.9rem;
        }
        
        /* Contato */
        .contact {
            background-color: #111;
        }
        
        .contact-content {
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
        }
        
        .contact-info, .contact-form {
            flex: 1;
            min-width: 300px;
        }
        
        .contact-info h3 {
            margin-bottom: 15px;
            color: #c1121f;
        }
        
        .contact-info p {
            margin-bottom: 10px;
        }
        
        .social-links {
            margin-top: 20px;
        }
        
        .social-links a {
            display: inline-block;
            margin-right: 15px;
            font-size: 1.5rem;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
        }
        
        .form-group input, .form-group textarea {
            width: 100%;
            padding: 10px;
            background-color: #1a1a1a;
            border: 1px solid #333;
            border-radius: 3px;
            color: white;
        }
        
        .form-group textarea {
            height: 150px;
            resize: vertical;
        }
        
        /* Rodapé */
        footer {
            background-color: #000;
            padding: 30px 0;
            text-align: center;
            border-top: 3px solid #c1121f;
        }
        
        footer p {
            margin-bottom: 10px;
        }
        
        /* Responsividade */
        @media (max-width: 768px) {
            .banner-content h2 {
                font-size: 2rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav ul li {
                margin: 5px 0;
            }
            
            .tour-item {
                flex-direction: column;
            }
            
            .tour-date {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <!-- Cabeçalho -->
    <header>
        <div class="container">
            <div class="logo">
                <h1>SLIPKNOT</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Início</a></li>
                    <li><a href="#about">Sobre</a></li>
                    <li><a href="#members">Membros</a></li>
                    <li><a href="#discography">Discografia</a></li>
                    <li><a href="#tour">Tour</a></li>
                    <li><a href="#contact">Contato</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Banner Principal -->
    <section id="home" class="banner">
        <div class="banner-content">
            <h2>Bem-vindo ao Mundo do Slipknot</h2>
            <p>A banda de metal mais intensa e visceral do planeta. Explore a história, a música e a loucura por trás das máscaras.</p>
            <a href="#about" class="btn">Descubra Mais</a>
        </div>
    </section>

    <!-- Sobre -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>Sobre a Banda</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <p>Slipknot é uma banda americana de metal formada em Des Moines, Iowa, em 1995. A banda é conhecida por suas apresentações energéticas e caóticas, máscaras distintivas e trajes uniformes, além de seu som agressivo que combina elementos de heavy metal, nu metal e metal alternativo.</p>
                    <p>Com nove membros, cada um numerado de 0 a 8, o Slipknot criou uma identidade visual única no mundo do metal. Sua formação atual inclui Corey Taylor (vocal), Mick Thomson e Jim Root (guitarras), Alessandro Venturella (baixo), Shawn "Clown" Crahan e Michael Pfaff (percussão), Craig Jones (samples), Sid Wilson (DJ) e Jay Weinberg (bateria).</p>
                    <p>Ao longo de sua carreira, o Slipknot lançou seis álbuns de estúdio, todos recebendo certificações de ouro ou platina. Seu álbum de estreia autointitulado (1999) e Iowa (2001) são considerados clássicos do gênero e influenciaram toda uma geração de músicos de metal.</p>
                </div>
                <div class="about-image">
                    <!-- Imagem representativa - na prática, seria uma imagem real da banda -->
                    <div style="width:100%; height:300px; background-color:#333; display:flex; align-items:center; justify-content:center; color:#aaa;">
                        IMAGEM DA BANDA SLIPKNOT
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Membros -->
    <section id="members" class="members">
        <div class="container">
            <div class="section-title">
                <h2>Membros</h2>
            </div>
            <div class="members-grid">
                <!-- Membro 1 -->
                <div class="member-card">
                    <div class="member-image" style="background-color: #333; display:flex; align-items:center; justify-content:center; color:#aaa;">
                        #8 - COREY TAYLOR
                    </div>
                    <div class="member-info">
                        <h3>Corey Taylor</h3>
                        <p>Vocalista principal do Slipknot e também frontman do Stone Sour. Conhecido por sua poderosa voz que varia entre guturais e melodias.</p>
                    </div>
                </div>
                
                <!-- Membro 2 -->
                <div class="member-card">
                    <div class="member-image" style="background-color: #333; display:flex; align-items:center; justify-content:center; color:#aaa;">
                        #7 - MICK THOMSON
                    </div>
                    <div class="member-info">
                        <h3>Mick Thomson</h3>
                        <p>Guitarrista conhecido por sua técnica precisa e agressiva. Usa uma máscara de executioner e é um dos membros mais antigos da banda.</p>
                    </div>
                </div>
                
                <!-- Membro 3 -->
                <div class="member-card">
                    <div class="member-image" style="background-color: #333; display:flex; align-items:center; justify-content:center; color:#aaa;">
                        #4 - JIM ROOT
                    </div>
                    <div class="member-info">
                        <h3>Jim Root</h3>
                        <p>Guitarrista que se juntou à banda em 1999. Também é membro do Stone Sour e conhecido por seu estilo único e riffs pesados.</p>
                    </div>
                </div>
                
                <!-- Membro 4 -->
                <div class="member-card">
                    <div class="member-image" style="background-color: #333; display:flex; align-items:center; justify-content:center; color:#aaa;">
                        #0 - SID WILSON
                    </div>
                    <div class="member-info">
                        <h3>Sid Wilson</h3>
                        <p>DJ e tecladista, conhecido por suas acrobacias no palco e samples eletrônicos que dão à banda sua sonoridade única.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Discografia -->
    <section id="discography" class="discography">
        <div class="container">
            <div class="section-title">
                <h2>Discografia</h2>
            </div>
            <div class="albums-grid">
                <!-- Álbum 1 -->
                <div class="album-card">
                    <div class="album-cover" style="background-color: #444; display:flex; align-items:center; justify-content:center; color:#aaa;">
                        SLIPKNOT (1999)
                    </div>
                    <div class="album-info">
                        <h3>Slipknot</h3>
                        <p>1999</p>
                    </div>
                </div>
                
                <!-- Álbum 2 -->
                <div class="album-card">
                    <div class="album-cover" style="background-color: #444; display:flex; align-items:center; justify-content:center; color:#aaa;">
                        IOWA (2001)
                    </div>
                    <div class="album-info">
                        <h3>Iowa</h3>
                        <p>2001</p>
                    </div>
                </div>
                
                <!-- Álbum 3 -->
                <div class="album-card">
                    <div class="album-cover" style="background-color: #444; display:flex; align-items:center; justify-content:center; color:#aaa;">
                        VOL. 3 (2004)
                    </div>
                    <div class="album-info">
                        <h3>Vol. 3: The Subliminal Verses</h3>
                        <p>2004</p>
                    </div>
                </div>
                
                <!-- Álbum 4 -->
                <div class="album-card">
                    <div class="album-cover" style="background-color: #444; display:flex; align-items:center; justify-content:center; color:#aaa;">
                        AHIG (2008)
                    </div>
                    <div class="album-info">
                        <h3>All Hope Is Gone</h3>
                        <p>2008</p>
                    </div>
                </div>
                
                <!-- Álbum 5 -->
                <div class="album-card">
                    <div class="album-cover" style="background-color: #444; display:flex; align-items:center; justify-content:center; color:#aaa;">
                        .5 (2014)
                    </div>
                    <div class="album-info">
                        <h3>.5: The Gray Chapter</h3>
                        <p>2014</p>
                    </div>
                </div>
                
                <!-- Álbum 6 -->
                <div class="album-card">
                    <div class="album-cover" style="background-color: #444; display:flex; align-items:center; justify-content:center; color:#aaa;">
                        WANYK (2019)
                    </div>
                    <div class="album-info">
                        <h3>We Are Not Your Kind</h3>
                        <p>2019</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Tour -->
    <section id="tour" class="tour">
        <div class="container">
            <div class="section-title">
                <h2>Próximos Shows</h2>
            </div>
            <div class="tour-dates">
                <!-- Show 1 -->
                <div class="tour-item">
                    <div class="tour-date">
                        <strong>15 OUT</strong>
                        <span>2023</span>
                    </div>
                    <div class="tour-info">
                        <h3>São Paulo, Brasil</h3>
                        <p>Allianz Parque</p>
                    </div>
                    <div class="tour-btn">
                        <a href="#" class="btn">Comprar Ingressos</a>
                    </div>
                </div>
                
                <!-- Show 2 -->
                <div class="tour-item">
                    <div class="tour-date">
                        <strong>18 OUT</strong>
                        <span>2023</span>
                    </div>
                    <div class="tour-info">
                        <h3>Rio de Janeiro, Brasil</h3>
                        <p>Estádio do Maracanã</p>
                    </div>
                    <div class="tour-btn">
                        <a href="#" class="btn">Comprar Ingressos</a>
                    </div>
                </div>
                
                <!-- Show 3 -->
                <div class="tour-item">
                    <div class="tour-date">
                        <strong>22 OUT</strong>
                        <span>2023</span>
                    </div>
                    <div class="tour-info">
                        <h3>Belo Horizonte, Brasil</h3>
                        <p>Estádio Mineirão</p>
                    </div>
                    <div class="tour-btn">
                        <a href="#" class="btn">Comprar Ingressos</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contato -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contato</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Entre em Contato</h3>
                    <p>Para mais informações sobre a banda, shows ou parcerias:</p>
                    <p>Email: info@slipknot.com</p>
                    <p>Telefone: (555) 123-4567</p>
                    
                    <div class="social-links">
                        <a href="#">Facebook</a>
                        <a href="#">Instagram</a>
                        <a href="#">Twitter</a>
                        <a href="#">YouTube</a>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Nome</label>
                            <input type="text" id="name" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Mensagem</label>
                            <textarea id="message" required></textarea>
                        </div>
                        
                        <button type="submit" class="btn">Enviar Mensagem</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Rodapé -->
    <footer>
        <div class="container">
            <p>&copy; 2023 Slipknot. Todos os direitos reservados.</p>
            <p>Este site é apenas para fins educacionais.</p>
        </div>
    </footer>
</body>
</html>
```

Características do Site

Este site sobre a banda Slipknot inclui:

1. Design responsivo que se adapta a diferentes tamanhos de tela
2. Cores temáticas baseadas na identidade visual da banda (preto, vermelho e cinza)
3. Seções organizadas:
   · Banner principal com chamada para ação
   · Sobre a banda
   · Membros atuais
   · Discografia completa
   · Datas de turnê
   · Formulário de contato
4. Elementos visuais que capturam a essência agressiva e intensa do Slipknot
5. Navegação intuitiva com menu fixo no topo

O código está pronto para ser executado diretamente em qualquer navegador. Para usar imagens reais, você precisaria substituir os placeholders por URLs de imagens reais da banda.
