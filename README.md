import os
from zipfile import ZipFile

# Criar estrutura de diretórios
base_dir = "portfolio"
img_dir = os.path.join(base_dir, "img")
os.makedirs(img_dir, exist_ok=True)

# HTML com dados da Vanessa
index_html_content = """<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
    <link rel="stylesheet" href="style.css">
    <title>Portfólio da Vanessa</title>
</head>
<body>
    <header class="container text-center">
        <img src="img/avatar-perfil.png" alt="avatar da Vanessa" class="rounded-circle" width="150" height="150">
        <p class="lead">Eu sou Vanessa_</p>
        <h1>Futura Médica Veterinária</h1>
        <p>Sou estudante do Ensino Médio e tenho o sonho de cursar Medicina Veterinária. 
        Tenho paixão por animais, pelo cuidado com a natureza e gosto muito de aprender coisas novas. 
        Esse portfólio mostra um pouco sobre mim!</p>
        <p>Minhas habilidades</p>
        <div>
            <p class="badge bg-secondary">Comunicativa</p>
            <p class="badge bg-secondary">Trabalho em equipe</p>
            <p class="badge bg-secondary">Boa ouvinte</p>
        </div>
    </header>
    <main class="container mt-5">
        <h2>Meus projetos</h2>
        <div class="row">
            <div class="col-md-4">
                <div class="card">
                    <img src="img/projeto-1.png" class="card-img-top" alt="Imagem de um projeto">
                    <div class="card-body">
                        <h5 class="card-title">Meu amor pelos animais</h5>
                        <p class="card-text">Um projeto onde conto sobre como surgiu meu interesse por medicina veterinária.</p>
                        <a href="#" class="btn btn-primary disabled">Em breve</a>
                    </div>
                </div>
            </div>
        </div>
    </main>
    <footer class="container py-5">
        <h2>Entre em contato</h2>
        <p class="my-5 text-center">© Copyright 2024. Produzido por Vanessa</p>
    </footer>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
"""

# CSS básico
style_css_content = """
body {
    background-color: #f5f5f5;
    font-family: 'Segoe UI', sans-serif;
}

header {
    margin-top: 2rem;
    margin-bottom: 2rem;
}

.lead {
    font-weight: bold;
    color: #6c757d;
}

footer {
    background-color: #e9ecef;
    padding: 2rem 1rem;
    text-align: center;
}
"""

# Escrever arquivos
with open(os.path.join(base_dir, "index.html"), "w", encoding="utf-8") as f:
    f.write(index_html_content)

with open(os.path.join(base_dir, "style.css"), "w", encoding="utf-8") as f:
    f.write(style_css_content)

# Criar imagens fictícias
placeholder = b"\x89PNG\r\n\x1a\n"  # Cabeçalho PNG
for name in ["avatar-perfil.png", "projeto-1.png"]:
    with open(os.path.join(img_dir, name), "wb") as f:
        f.write(placeholder)

# Criar ZIP
with ZipFile("portfolio-vanessa.zip", "w") as zipf:
    for folder, _, files in os.walk(base_dir):
        for file in files:
            path = os.path.join(folder, file)
            zipf.write(path, os.path.relpath(path, base_dir))
