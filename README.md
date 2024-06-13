# zip_code
import zipfile

# Caminho para salvar o arquivo zip
zip_path = "/mnt/data/folha-de-pagamento-apresentacao.zip"

# Conteúdo do arquivo index.html
index_html = """<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Resumo do Cálculo da Folha de Pagamento</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        .container {
            width: 80%;
            margin: auto;
            overflow: hidden;
        }
        header {
            background: #35424a;
            color: #ffffff;
            padding-top: 30px;
            min-height: 70px;
            border-bottom: #e8491d 3px solid;
        }
        header h1 {
            margin: 0;
            text-align: center;
            text-transform: uppercase;
            font-size: 24px;
        }
        .showcase {
            text-align: center;
            padding: 20px;
            background: #ffffff;
            margin-top: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        .showcase img {
            max-width: 100%;
            height: auto;
        }
        .content {
            padding: 20px;
            background: #ffffff;
            margin-top: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        .content h2 {
            text-align: center;
            padding-bottom: 10px;
        }
        .content p {
            line-height: 1.6;
        }
        footer {
            text-align: center;
            padding: 20px;
            margin-top: 20px;
            color: #ffffff;
            background-color: #35424a;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Resumo do Cálculo da Folha de Pagamento</h1>
        </div>
    </header>

    <section class="showcase container">
        <img src="minha_foto.jpg" alt="Descrição da imagem">
    </section>

    <section class="content container">
        <h2>Coleta de Informações</h2>
        <p>Dados dos Funcionários, Frequência de Pagamento, Contratos e Acordos.</p>

        <h2>Cálculo dos Vencimentos</h2>
        <p>Salário Base, Horas Extras, Adicionais.</p>

        <h2>Benefícios</h2>
        <p>Vale-Transporte, Vale-Alimentação/Refeição, Assistência Médica e Odontológica.</p>

        <h2>Descontos Obrigatórios</h2>
        <p>INSS, IRRF, FGTS.</p>

        <h2>Descontos Facultativos</h2>
        <p>Contribuição Sindical, Empréstimos Consignados, Planos de Previdência Privada.</p>

        <h2>Cálculo do Salário Líquido</h2>
        <p>Salário Bruto, Descontos Totais, Salário Líquido.</p>

        <h2>Emissão dos Recibos</h2>
        <p>Holerite, Pagamento.</p>

        <h2>Obrigações Acessórias</h2>
        <p>CAGED, DIRF, RAIS.</p>

        <h2>Exemplo de Cálculo</h2>
        <p>
            1. Salário Base: R$ 3.000,00<br>
            2. Horas Extras: 10 horas a 50% (10 x (R$ 3.000,00 / 220) x 1,5) = R$ 204,55<br>
            3. Vale-Transporte: R$ 180,00 (6% do salário base)<br>
            4. INSS: R$ 330,00 (11% do salário bruto para simplificação)<br>
            5. IRRF: R$ 70,00 (valor fictício para exemplo)<br>
               - Salário Bruto: R$ 3.204,55<br>
               - Descontos Totais: R$ 580,00 (R$ 180,00 + R$ 330,00 + R$ 70,00)<br>
               - Salário Líquido: R$ 2.624,55
        </p>
    </section>

    <footer>
        <p>Resumo do Cálculo da Folha de Pagamento &copy; 2024</p>
    </footer>
</body>
</html>"""

# Criação do arquivo zip
with zipfile.ZipFile(zip_path, 'w') as zipf:
    zipf.writestr('index.html', index_html)
    # Adicionando uma imagem placeholder
    zipf.writestr('minha_foto.jpg', b'\x89PNG\r\n\x1a\n\x00\x00\x00\rIHDR\x00\x00\x00\x10\x00\x00\x00\x10\x08\x06\x00\x00\x00\x1f\xf3\xffa\x00\x00\x00\x19tEXtSoftware\x00Adobe ImageReadyq\xc9e<\x00\x00\x00UIDATx\xda\xcc\x93A\x0e\x80 \x0c\x04\r\xc4\xfd\xaf\xb2\xdb3P,\x9a\x9dK$\xe2\xd0\xf6u\x02*\xdaC\n\xcf\x07\xe2s9\xb8\xf7q\xe1\xda\x1c2.\xfa\xb8\xc7\xa1\x8d]\xc4k\x8c\xb5\xf2\xff\x00\x00\x00\x00IEND\xaeB`\x82')

zip_path
