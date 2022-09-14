<?php include "./cabecalho.php"; ?>
    <h1>Contato!</h1>

<?php
    if(!empty($_POST) && isset($_POST)){
        if (empty($_POST["email"])){
            ?>
            <div class="alert alert-danger">
                O e-mail deve ser informado!
            </div>
        <?php
        }else if(empty($_POST["nome"])){
            ?>
            <div class="alert alert-danger">
                O nome deve ser informado!
            </div>
        }
        <?php
        
        }else{
            ?>
            <div class="alert alert-success">
                Sua Reclamação foi enviada!
            </div>
            <?php
        }
        }else{
            echo "não veio informação do POST";
            }

        ?>

    <form action="./contato.php" method="post">
        <div class="form-group col-4 offset-4">
            <label> Nome </label>
            <input type="text" class="form-control" name="nome"/>
        </div>
        <div class="form-group col-4 offset-4">
            <label> E-mail </label>
            <input type="email" require class="form-control" name="email"/>
        </div>
        <div class="form-group col-4 offset-4">
            <Label>Observação</Label>
            <textarea class="form-control " name="obs"></textarea>
        </div>  
        <br>
        <div class="form-group col-4 offset-4">
            <button type="submit" class="btn btn-warning "> Enviar Dados</button>
        </div>

    </form>
  

<?php include "./rodape.php"; ?>
