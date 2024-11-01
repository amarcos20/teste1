<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instruções de Computadores - Guia Interativo</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            color: #333;
        }
        header {
            background-color: #0073e6;
            color: white;
            padding: 20px;
            text-align: center;
        }
        nav {
            display: flex;
            justify-content: center;
            background-color: #005bb5;
        }
        nav a {
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            display: block;
        }
        nav a:hover {
            background-color: #003f7f;
        }
        main {
            padding: 20px;
            max-width: 800px;
            margin: auto;
        }
        section {
            margin-bottom: 20px;
            border-radius: 8px;
            background-color: #fff;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        h2 {
            cursor: pointer;
            padding: 15px;
            background-color: #0073e6;
            color: white;
            margin: 0;
        }
        .content {
            display: none;
            padding: 15px;
        }
        .content p, .content ul {
            margin: 10px 0;
        }
        .show {
            display: block;
        }
        footer {
            background-color: #0073e6;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>

<header>
    <h1>Guia Interativo de Instruções de Computadores</h1>
    <p>Explore o conjunto de instruções e a arquitetura dos computadores</p>
</header>

<nav>
    <a href="#intro">Introdução</a>
    <a href="#isa">ISA</a>
    <a href="#mips">Instruções MIPS</a>
    <a href="#example">Exemplo</a>
</nav>

<main>
    <section id="intro">
        <h2 onclick="toggleContent(this)">O que é uma Instrução de Computador?</h2>
        <div class="content">
            <p>Instruções de computador são comandos binários que informam ao processador como executar uma operação específica. Elas são a base da programação de baixo nível e servem como interface entre o software e o hardware.</p>
        </div>
    </section>

    <section id="isa">
        <h2 onclick="toggleContent(this)">Instruction Set Architecture (ISA)</h2>
        <div class="content">
            <p>A <strong>Instruction Set Architecture (ISA)</strong> define o conjunto de instruções que um processador pode executar. Exemplos de ISA incluem x86, ARM e MIPS.</p>
            <p>No MIPS, as instruções são divididas em três tipos principais:</p>
            <ul>
                <li><strong>Tipo R (Register)</strong>: Operações que utilizam apenas registradores, como somas e subtrações.</li>
                <li><strong>Tipo I (Immediate)</strong>: Instruções que incluem valores constantes, como carregamento e armazenamento de dados.</li>
                <li><strong>Tipo J (Jump)</strong>: Instruções de salto, usadas para controle de fluxo.</li>
            </ul>
        </div>
    </section>

    <section id="mips">
        <h2 onclick="toggleContent(this)">Principais Instruções no MIPS</h2>
        <div class="content">
            <ul>
                <li><strong>add $d, $s, $t</strong>: Soma os valores dos registradores $s e $t e armazena em $d.</li>
                <li><strong>sub $d, $s, $t</strong>: Subtrai o valor de $t do valor de $s e armazena em $d.</li>
                <li><strong>lw $t, offset($s)</strong>: Carrega uma palavra da memória no endereço base + offset para o registrador $t.</li>
                <li><strong>sw $t, offset($s)</strong>: Armazena uma palavra do registrador $t para a memória no endereço base + offset.</li>
                <li><strong>j target</strong>: Salta para o endereço especificado por target.</li>
            </ul>
        </div>
    </section>

    <section id="example">
        <h2 onclick="toggleContent(this)">Exemplo: Como Funciona a Instrução "lw"</h2>
        <div class="content">
            <p>A instrução <strong>lw $t, offset($s)</strong> (load word) é usada para carregar dados da memória para um registrador. Ela calcula o endereço com base no valor do registrador $s e no offset, e armazena o valor no registrador $t.</p>
            <p><em>Exemplo</em>: <code>lw $18, -132($19)</code> carrega o valor da posição de memória <code>Reg[19] - 132</code> para o registrador $18.</p>
        </div>
    </section>
</main>

<footer>
    <p>&copy; 2024 Guia Universitário de Instruções de Computadores</p>
</footer>

<script>
    function toggleContent(element) {
        const content = element.nextElementSibling;
        content.classList.toggle('show');
    }
</script>

</body>
</html>
