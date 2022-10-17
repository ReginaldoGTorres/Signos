<!doctype html>
	<html lang="pt-BR">
	<head>
	    <meta charset="utf-8">
	    <meta name="viewport" content="width=device-width, initial-scale=1">
	    <title> RGT │ Fórum 1 - Programação Web </title>
	

	    <style>
	        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;200;400;500;600;700&display=swap');
	

	        * {
	            margin: 0;
	            border: 0;
	            box-sizing: border-box;
	            font-family: "Roboto", sans-serif;
	        }
	

	        body {
	            background: linear-gradient(50deg, rgba(125,165,150,1) 50%, rgba(248,185,150,1) 90%);
	            min-height: 100vh;
	            min-width: 100vh;
	            display: flex;
	            align-items: center;
	            justify-content: center;
	        }
	

	        .container {
	            background: white;
	            max-width: 600px;
	            padding: 2rem;
	            box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.2);
	            border-radius: 8px;
	        }
	

	        h2{
	            font-weight: 600;
	            font-size: 30px;
	            margin-bottom: 2rem;
	            position: relative;
	        }
	

	        h2::first-letter{
	            text-transform: uppercase;
	        }
	

	        h2::before {
	            content: '';
	            position: absolute;
	            height: 4px;
	            width: 25px;
	            bottom: 3px;
	            left: 0;
	            border-radius: 8px;
	            background: linear-gradient(50deg, rgba(125,165,150,1) 50%, rgba(248,185,150,1) 90%);
	        }
	

	        p{
	            text-align: justify;
	        }
	

	        button{
	            margin-top: 2rem;
	            padding: 0.4rem;
	            width: 100%;
	            background: linear-gradient(50deg, rgba(125,165,150,1) 50%, rgba(248,185,150,1) 90%);
	            cursor: pointer;
	            color: white;
	            font-size: 0.9rem;
	            font-weight: 300;
	            border-radius: 4px;
	            transition: all 0.3s ease;
	        }
	

	        button[type="submit"]:hover {
	            letter-spacing: 0.5px;
	background: linear-gradient(50deg, rgba(125,165,150,1) 50%, rgba(248,185,150,1) 90%);
	        }
	

	

	        footer{
	            background: red(255, 255, 255, 0.455);
	            display: flex;
	            align-items: center;
	            position: fixed;
	            justify-content: center;
	            bottom:0;
	            left: 0;
	            margin: 0 auto;
	            width: 100%;
	            height: 25px;
	        }
	

	        footer h4{
	            font-weight: 200;
	            font-size: 15px;
	            color: rgba(0, 0, 0, 0.7);
	        }
	

	        @media (max-width: 768px) {
	            body{
	                min-width: auto;
	            }
	        }
	

	    </style>
	    
	</head>
	

	<body>
	    <main class="container">
	        <?php
	        $Nome = $_POST['nomePess'];
	        $dtaNasc = $_POST['dataNasc'];
	        $date = new DateTime($dtaNasc);
	        $dtaSigno = $date->format('m-d');
	        $xml = simplexml_load_file('signos.xml');
	    
	        echo '<h2>' . $Nome.', o seu signo é:</h2>';
	        foreach ($xml->signo as $retorno) :
	        if ($dtaSigno >= $retorno->dtaInicio and $dtaSigno <= $retorno->dtaFinal) {
	        echo '<h1>' . $retorno->descSigno . '</h1>';
	        echo '<p>' . nl2br($retorno->personalidade) . '<p>';
	        }
	        endforeach;       
	        ?>
	

	        <button onclick="history.go(-1);">Voltar</button>
	        
	    </main>
	

	    <footer>
	        <h4>2022 - RGT</h4>
	    </footer>
	    
	</body>
	</html>
