# 2 - Selectores e Especificidade

~~~html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Multiplos Estilos Em Css</title>
</head>
<body>
    <!-- Classes CSS -->
    <h1 id="titulo-principal">Título da Página</h1>

    <!-- Ids -->
    <p class="destaque importante">Este texto é importante e destacado.</p>

    <!-- Seletores Combinados -->
    <div class="container">
        <p class="destaque">Texto dentro de um container.</p>
    </div>

    <!-- Herança -->
    <div class="container">
        <h1>Título</h1>
        <p>Parágrafo</p>
    </div>
</body>
</html>
~~~