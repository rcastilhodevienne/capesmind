<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CAPES MIND</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f9fdf9;
      color: #333;
    }
    header {
      background-color: #2ecc71;
      color: white;
      padding: 10px 20px;
      text-align: center;
      font-size: 24px;
      font-weight: bold;
    }
    .screen {
      display: none;
      padding: 20px;
    }
    .screen.active {
      display: block;
    }
    .btn {
      display: inline-block;
      margin: 10px 5px;
      padding: 15px 25px;
      font-size: 16px;
      color: white;
      background: #2ecc71;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      text-align: center;
      text-decoration: none;
    }
    .btn:hover {
      background: #27ae60;
    }
    input, textarea, select {
      display: block;
      width: 80%;
      margin: 10px auto;
      padding: 10px;
      font-size: 16px;
      border: 1px solid #ddd;
      border-radius: 5px;
    }
    ul {
      margin: 20px auto;
      padding: 0;
      list-style: none;
      width: 80%;
    }
    ul li {
      margin: 10px 0;
      padding: 10px;
      background: #ecf9ec;
      border: 1px solid #ddd;
      border-radius: 5px;
    }
    nav {
      position: fixed;
      bottom: 0;
      width: 100%;
      background: #f1f1f1;
      display: flex;
      justify-content: space-around;
      padding: 10px 0;
      border-top: 1px solid #ddd;
    }
    nav button {
      flex: 1;
      padding: 10px;
      font-size: 14px;
      cursor: pointer;
      border: none;
      background: transparent;
      color: #2ecc71;
    }
    nav button.active {
      font-weight: bold;
      border-top: 2px solid #2ecc71;
    }
  </style>
</head>
<body>
  <header>CAPES MIND</header>

  <!-- Splash Screen -->
  <div id="splash" class="screen active">
    <h1>Bem-vindo ao CAPES MIND</h1>
    <p>O portal que conecta ciência, tecnologia e você.</p>
    <button class="btn" onclick="navigateTo('login')">Iniciar</button>
  </div>

  <!-- Login Screen -->
  <div id="login" class="screen">
    <h2>Login</h2>
    <input type="email" placeholder="E-mail" />
    <input type="password" placeholder="Senha" />
    <button class="btn" onclick="navigateTo('home')">Entrar</button>
  </div>

  <!-- Home Screen -->
  <div id="home" class="screen">
    <h2>Home</h2>
    <p>Escolha o que deseja fazer:</p>
    <button class="btn" onclick="navigateTo('busca')">Buscar Artigos</button>
    <button class="btn" onclick="navigateTo('recomendacoes')">Recomendações</button>
    <button class="btn" onclick="navigateTo('publicar')">Publicar Artigo</button>
    <button class="btn" onclick="navigateTo('perfil')">Meu Perfil</button>
  </div>

  <!-- Busca Screen -->
  <div id="busca" class="screen">
    <h2>Buscar Artigos</h2>
    <input type="text" placeholder="Digite o termo de busca" />
    <select>
      <option value="todas">Todas as Categorias</option>
      <option value="saude">Saúde</option>
      <option value="tecnologia">Tecnologia</option>
      <option value="educacao">Educação</option>
    </select>
    <button class="btn" onclick="navigateTo('resultado')">Buscar</button>
  </div>

  <!-- Resultado Screen -->
  <div id="resultado" class="screen">
    <h2>Resultados da Busca</h2>
    <ul>
      <li>Artigo 1: O impacto da IA na saúde</li>
      <li>Artigo 2: Educação na era digital</li>
      <li>Artigo 3: Sustentabilidade e inovação</li>
    </ul>
    <button class="btn" onclick="navigateTo('busca')">Nova Busca</button>
    <button class="btn" onclick="navigateTo('home')">Voltar ao Início</button>
  </div>

  <!-- Recomendações Screen -->
  <div id="recomendacoes" class="screen">
    <h2>Recomendações para Você</h2>
    <p>Baseado no seu histórico:</p>
    <ul>
      <li>Artigo: Avanços na biotecnologia</li>
      <li>Artigo: A revolução dos veículos elétricos</li>
    </ul>
    <button class="btn" onclick="navigateTo('home')">Voltar ao Início</button>
  </div>

  <!-- Publicar Artigo Screen -->
  <div id="publicar" class="screen">
    <h2>Publicar Artigo</h2>
    <input type="text" placeholder="Título do Artigo" />
    <textarea placeholder="Resumo do Artigo"></textarea>
    <button class="btn" onclick="alert('Artigo enviado com sucesso!')">Enviar</button>
    <button class="btn" onclick="navigateTo('home')">Voltar ao Início</button>
  </div>

  <!-- Perfil Screen -->
  <div id="perfil" class="screen">
    <h2>Meu Perfil</h2>
    <p>Nome: João da Silva</p>
    <p>E-mail: joao@email.com</p>
    <p>Artigos publicados: 5</p>
    <button class="btn" onclick="navigateTo('home')">Voltar ao Início</button>
  </div>

  <!-- Navegação -->
  <nav>
    <button id="nav-home" onclick="navigateTo('home')">Home</button>
    <button id="nav-busca" onclick="navigateTo('busca')">Buscar</button>
    <button id="nav-recomendacoes" onclick="navigateTo('recomendacoes')">Recomendações</button>
    <button id="nav-publicar" onclick="navigateTo('publicar')">Publicar</button>
    <button id="nav-perfil" onclick="navigateTo('perfil')">Perfil</button>
  </nav>

  <!-- Script -->
  <script>
    function navigateTo(screenId) {
      document.querySelectorAll('.screen').forEach(screen => screen.classList.remove('active'));
      document.querySelector(`#${screenId}`).classList.add('active');
      document.querySelectorAll('nav button').forEach(button => button.classList.remove('active'));
      const activeNav = document.querySelector(`#nav-${screenId}`);
      if (activeNav) activeNav.classList.add('active');
    }
  </script>
</body>
</html>
