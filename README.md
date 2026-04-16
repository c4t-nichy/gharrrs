<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Currículo</title>
    <style>
        :root {
            --primary: #2d3436;
            --accent: #0984e3;
            --bg: #dfe6e9;
            --text: #2d3436;
        }

        body.dark-mode {
            --primary: #dfe6e9;
            --accent: #74b9ff;
            --bg: #2d3436;
            --text: #f5f6fa;
        }

        body {
            font-family: 'Segoe UI', sans-serif;
            background-color: var(--bg);
            color: var(--text);
            transition: 0.3s;
            display: flex;
            justify-content: center;
            padding: 20px;
        }

        .container {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            padding: 40px;
            border-radius: 15px;
            max-width: 800px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }

        h1 { color: var(--accent); margin-bottom: 5px; }
        .subtitle { font-style: italic; margin-bottom: 20px; opacity: 0.8; }

        .section { margin-bottom: 25px; }
        h3 { border-bottom: 2px solid var(--accent); padding-bottom: 5px; }

        .skill-tag {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            margin: 5px;
            font-size: 0.9em;
            cursor: pointer;
            transition: transform 0.2s;
        }

        .skill-tag:hover { transform: scale(1.1); }

        button {
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 10px;
            cursor: pointer;
            border-radius: 5px;
            border: none;
            background: var(--accent);
            color: white;
        }
    </style>
</head>
<body>

    <button onclick="toggleTheme()">Alternar Modo</button>

    <div class="container">
        <header>
            <h1>Nicolly Sovenil</h1>
            <p class="subtitle">Desenvolvedor Python & Entusiasta de Design Visual</p>
        </header>

        <div class="section">
            <h3>Sobre Mim</h3>
            <p>Combinando a lógica da programação com a sensibilidade do desenho, busco criar soluções que sejam funcionais e visualmente impactantes. Estudante dedicado de novas tecnologias e comunicação global.</p>
        </div>

        <div class="section">
            <h3>Habilidades Principais</h3>
            <div id="skills-container">
                <span class="skill-tag">Python (Básico ao Intermediário)</span>
                <span class="skill-tag">Inglês (Conversação/Leitura)</span>
                <span class="skill-tag">Desenho Artístico e Digital</span>
                <span class="skill-tag">Lógica de Programação</span>
                <span class="skill-tag">UI/UX Design</span>
                <span class="skill-tag">Git & GitHub</span>
            </div>
        </div>

        <div class="section">
            <h3>Formação & Cursos</h3>
            <ul>
                <li><strong>Curso de Python:</strong> Automação, análise de dados e fundamentos.</li>
                <li><strong>Estudo de Desenho:</strong> Anatomia, perspectiva e teoria das cores.</li>
                <li><strong>Inglês:</strong> Foco em documentação técnica e comunicação.</li>
            </ul>
        </div>

        <div class="section">
            <h3>Projetos</h3>
            <p><em>"Script de Automação em Python para Organização de Arquivos"</em></p>
            <p><em>"Portfólio de Ilustrações Digitais"</em></p>
        </div>
    </div>

    <script>
        function toggleTheme() {
            document.body.classList.toggle('dark-mode');
        }

        // Pequena interação dinâmica ao clicar nas habilidades
        document.querySelectorAll('.skill-tag').forEach(tag => {
            tag.addEventListener('click', () => {
                alert("Você clicou na habilidade: " + tag.innerText);
            });
        });
    </script>
</body>
</html>
