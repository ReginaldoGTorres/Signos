<!doctype html>
<html lang="pt-BR">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>RGT │ Fórum 1 - Programação Web</title>

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
            font-weight: 500;
            margin-bottom: 2rem;
            position: relative;
        }

        h2::before {
            content: '';
            position: absolute;
            height: 4px;
            width: 235px;
            bottom: 4px;
            left: 0;
            border-radius: 8px;
            background: linear-gradient(50deg, rgba(125,165,150,1) 50%, rgba(248,185,150,1) 90%);
        }

        form {
            display: flex;
            flex-direction: column;
        }

        .input-field {
            position: relative;
        }

        form .input-field:first-child {
            margin-bottom: 1.5rem;
        }

        .input-field .underline::before {
            content: '';
            position: absolute;
            height: 1px;
            width: 50%;
            bottom: -5px;
            left: 0;
            background: rgba(0, 0, 0, 0.2);
        }

        .input-field .underline::after {
            content: '';
            position: absolute;
            height: 1px;
            width: 50%;
            bottom: -5px;
            left: 0;
            background: linear-gradient(50deg, rgba(125,165,150,1) 50%, rgba(248,185,150,1) 90%);
            transform: scaleX(0);
            transition: all .3s ease-in-out;
            transform-origin: left;
        }

        .input-field input:focus ~ .underline::after {
            transform: scaleX(1);
        }

        .input-field input {
            outline: none;
            font-size: 1.1rem;
            color: rgba(0, 0, 0, 0.7);
            width: 60%;
        }

        .input-field input::placeholder {
            color: rgba(0, 0, 0, 0.7);
        }

        button{
            margin-top: 2rem;
            padding: 0.4rem;
            width: 100%;
            background: linear-gradient(80deg, rgba(125,165,150,1) 20%, rgba(248,185,150,1) 90%);
            cursor: pointer;
            color: black;
            font-size: 1.5rem;
            font-weight: 400;
            border-radius: 4px;
            transition: all 0.3s ease;
        }

        button[type="submit"]:hover {
            letter-spacing: 0.5px;
            background: linear-gradient(80deg, rgba(125,165,150,1) 20%, rgba(248,185,150,1) 90%);
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
            color: red(0, 0, 0, 5.8);
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
        <h1>Fórum 1 – Programação Web</h1>
        <h2>Qual é o seu signo?</h2>
        <form action="signos.php" method="post">
            <div class="input-field">
                <input type="text" class="form-control" id="floatingInput" name="nomePess" placeholder="Digite o seu nome" required>
                <div class="underline"></div>
            </div>
            <div class="input-field">
                <input type="date" class="form-control" id="floatingInput" name="dataNasc" placeholder=" Sua data" required>
                <div class="underline"></div> 
            </div> Digite a sua data de nascimento
            <button type="submit" value="submit">Click Aqui!</button>
        </form>
      </form>
    </main>

    <footer>
        <h4>2022 - RGT</h4>
    </footer>

</body>
</html>
