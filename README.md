<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Designer de Roupeiro</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #333; /* Fundo cinza escuro */
            color: white; /* Cor do texto */
            margin: 0;
            padding: 20px;
            display: flex;
            flex-direction: column; /* Alinha os itens em coluna */
            justify-content: flex-start; /* Alinha o conteúdo no topo */
            align-items: center; /* Centraliza horizontalmente */
            height: 100vh; /* Altura total da tela */
        }
        h1 {
            text-align: center;
            margin-bottom: 20px; /* Aumenta o espaço entre o título e o formulário */
        }
        form {
            max-width: 400px;
            margin: 0 auto;
            padding: 20px;
            border-radius: 10px;
            background-color: rgba(255, 255, 255, 0.1); /* Fundo semi-transparente */
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5); /* Sombra para profundidade */
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold; /* Negrito para os rótulos */
        }
        input[type="number"] {
            width: calc(100% - 20px); /* Ajusta a largura para incluir padding */
            padding: 10px;
            margin-bottom: 15px; /* Aumenta o espaço entre os inputs */
            border: 1px solid #ccc;
            border-radius: 5px;
            background-color: #444; /* Fundo dos inputs */
            color: white; /* Cor do texto dos inputs */
        }
        button {
            width: 100%;
            padding: 10px;
            background-color: #ee9e26;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px; /* Aumenta o tamanho da fonte do botão */
        }
        button:hover {
            background-color: #ee9e26; /* Cor do botão ao passar o mouse */
        }
    </style>
</head>
<body>
    <h1>Gerador de Roupeiros</h1>
    <form id="wardrobeForm">
        <table>
            <tr>
                <td><label for="height">Altura</label></td>
                <td><input type="number" id="height" required></td>
            </tr>
            <tr>
                <td><label for="width">Largura</label></td>
                <td><input type="number" id="width" required></td>
            </tr>
            <tr>
                <td><label for="depth">Profundidade</label></td>
                <td><input type="number" id="depth" required></td>
            </tr>
            <tr>
                <td><label for="modules">Nr de módulos</label></td>
                <td><input type="number" id="modules" required></td>
            </tr>
        </table>
        <br>
        <button type="button" onclick="generateWardrobe()">Gerar Roupeiro</button>
    </form>

    <script>
        function generateWardrobe() {
            const width = document.getElementById('width').value;
            const modules = document.getElementById('modules').value;

            // Armazena os valores no localStorage
            localStorage.setItem('wardrobeWidth', width);
            localStorage.setItem('wardrobeModules', modules);

            // Redireciona para a página de resultados
            window.location.href = 'resultado.html';
        }
    </script>
</body>
</html>
