# Formulário de Contato Web

Projeto de formulário desenvolvido com HTML5 e CSS3, aplicando boas práticas de estruturação, validação de dados e organização de código.

## 🚀 Tecnologias Utilizadas
- HTML5
- CSS3

## 📌 Funcionalidades
- Validação de campos obrigatórios
- Campo de CPF com verificação de padrão
- Layout organizado com Fieldset
- Interface estilizada com CSS

## 📷 Preview do Projeto
![Preview](preview.png)


<style>
    body {
        font-family: Arial, Helvetica, sans-serif;
        background-color: #f4f6f9;
        display: flex;
        justify-content: center;
        padding: 40px;
    }

    form {
        background-color: #6cb3fb;
        padding: 30px;
        border-radius: 8px;
        width: 500px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    }

    fieldset {
        border: 1px solid #ddd;
        border-radius: 6px;
        padding: 15px;
        margin-bottom: 20px;
    }

    legend {
        font-weight: bold;
        padding: 0 10px;
        color: #333;
    }

    label {
        display: block;
        margin-top: 10px;
        margin-bottom: 5px;
        font-weight: 600;
        color: #444;
    }

    input, select, textarea {
        width: 100%;
        padding: 8px;
        border-radius: 4px;
        border: 1px solid #ccc;
        font-size: 14px;
        box-sizing: border-box;
        transition: border 0.3s;
    }

    input:focus, select:focus, textarea:focus {
        border-color: #007bff;
        outline: none;
    }

    textarea {
        resize: vertical;
    }

    button {
        padding: 10px 15px;
        border: none;
        border-radius: 4px;
        font-size: 14px;
        cursor: pointer;
        margin-right: 10px;
        transition: background 0.3s;
    }

    button[type="submit"] {
        background-color: #007bff;
        color: white;
    }

    button[type="submit"]:hover {
        background-color: #0056b3;
    }

    button[type="reset"] {
        background-color: #6c757d;
        color: white;
    }

    button[type="reset"]:hover {
        background-color: #545b62;
    }
</style>

</head>
<body>

<form action="/pagina-processa-dados-do-form" method="post">

    <fieldset>
        <legend>Dados Gerais</legend>

        <label for="nome">Nome:</label>
        <input type="text" id="nome" name="nome" minlength="3" required />

        <label for="data_nascimento">Data de Nascimento:</label>
        <input type="date" id="data_nascimento" name="data_nascimento" required />

        <label for="cpf">CPF:</label>
        <input type="text" id="cpf" name="cpf" pattern="\d{11}" maxlength="11" placeholder="Apenas números" required />
    </fieldset>

    <fieldset>
        <legend>Endereço</legend>

        <label for="tipo_endereco">Tipo:</label>
        <select id="tipo_endereco" name="tipo_endereco" required>
            <option value="">Selecione</option>
            <option value="rua">Rua</option>
            <option value="estrada">Estrada</option>
            <option value="rodovia">Rodovia</option>
            <option value="outros">Outros</option>
        </select>

        <label for="logradouro_endereco">Logradouro:</label>
        <input type="text" id="logradouro_endereco" name="logradouro_endereco" required />

        <label for="numero_endereco">Número:</label>
        <input type="text" id="numero_endereco" name="numero_endereco" required />

        <label for="complemento_endereco">Complemento:</label>
        <input type="text" id="complemento_endereco" name="complemento_endereco" />
    </fieldset>

    <fieldset>
        <legend>Fale Conosco</legend>

        <label for="msg">Mensagem:</label>
        <textarea id="msg" name="msg" rows="4" required></textarea>
    </fieldset>

    <fieldset>
        <button type="submit">Enviar sua mensagem</button>
        <button type="reset">Limpar o formulário</button>
    </fieldset>

</form>

</body>
</html>
