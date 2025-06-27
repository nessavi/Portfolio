<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <Meu Portfólio>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <img src="[https://cdn-icons-png.flaticon.com/512/4140/4140037.png](https://github.com/nessavi/Portfolio/blob/main/Foto%20perfil.jpeg)" alt="Avatar de Vanessa" class="avatar">
    <h2>Eu sou Vanessa_</h2>
    <h1>Futura Médica Veterinária</h1>
    <p>
      Sou estudante do Ensino Médio e tenho o sonho de cursar Medicina Veterinária. Tenho paixão por animais, pelo cuidado com a natureza e gosto muito de aprender coisas novas. Esse portfólio mostra um pouco sobre mim
    </p>
    <h3>Minhas habilidades</h3>
    <div class="skills">
      <span>Comunicação</span>
      <span>Trabalho em grupo</span>
      <span>Boa ouvinte</span>
      <span>Criativa</span>
    </div>
  </header>

  <main>
    <h2>Meus projetos</h2>
    <section class="projects">

      <div class="card">
        <img src="https://via.placeholder.com/300x180/FFB6C1/000000?text=Minha+Biblioteca" alt="Biblioteca">
        <h3>Minha Biblioteca: Uma Webpage Personalizada</h3>
        <p>Uma página web que apresenta uma lista dos meus livros favoritos, com autores, datas e links para compra.</p>
      </div>

      <div class="card">
        <img src="https://via.placeholder.com/300x180/000000/00FFFF?text=Inteligência+Artificial" alt="IA">
        <h3>Decidindo o Futuro: Uma Jornada Interativa sobre a Inteligência Artificial</h3>
        <p>Um jogo interativo explorando os impactos da IA na sociedade, onde o jogador faz escolhas e reflete sobre o futuro.</p>
      </div>

      <div class="card">
        <img src="https://via.placeholder.com/300x180/001f3f/7FDBFF?text=Universo+Scratch" alt="Universo">
        <h3>Explorando o Universo: Uma Aventura Interativa em Astronomia com Scratch</h3>
        <p>Uma experiência interativa educativa sobre astronomia criada com Scratch, com botões e animações divertidas.</p>
      </div>

    </section>
  </main>
</body>
</html>
body {
  font-family: 'Arial', sans-serif;
  margin: 0;
  padding: 0;
  background: #f6f9fc;
  color: #1a1a1a;
  text-align: center;
}

header {
  padding: 40px 20px;
}

.avatar {
  width: 100px;
  border-radius: 50%;
  margin-bottom: 15px;
}

h1 {
  font-size: 2.5rem;
  color: #14213d;
}

h2 {
  font-size: 1.8rem;
  margin-top: 10px;
}

h3 {
  font-size: 1.2rem;
  margin-top: 20px;
}

.skills {
  margin-top: 10px;
}

.skills span {
  background: #dee2e6;
  padding: 8px 12px;
  border-radius: 20px;
  margin: 5px;
  display: inline-block;
}

main {
  padding: 20px;
}

.projects {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
  margin-top: 20px;
}

.card {
  background: white;
  border-radius: 10px;
  width: 300px;
  padding: 15px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
  text-align: left;
}

.card img {
  width: 100%;
  border-radius: 8px;
}

.card h3 {
  margin-top: 10px;
  color: #14213d;
}

.card p {
  font-size: 0.95rem;
  color: #555;
}
