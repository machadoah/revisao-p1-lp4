 # Revisão CRUD PHP ![ForsakenWorldFwGIF](https://github.com/machadoah/revisao-p1-lp4/assets/96703665/6bf36119-d11c-4688-9d38-f9094353c520)

## Laravel primeiros passos
1. Instalar o [git](https://git-scm.com/downloads).
2. Instalar o [composer](https://getcomposer.org/download/).
3. Instalar o [Xampp](https://www.apachefriends.org/pt_br/index.html).

## Criando projeto MVC
No Git Bash ou no terminal do VSCode ou qualquer IDE, execute o comando:

```
composer create-project --prefer-dist laravel/laravel <nomedoprojeto>
```
**ATENÇÃO:**
**<nomedoprojeto>** define o nome, na execução do comando ele deve estar fora do simbolo de maior e menor.

### Iniciando o projeto
Agora é necessário criar o banco e iniciar o MySQL e o Apache no Xampp.

Para startar o projeto é só executar o comando:

```
php artisan serve
```

A criação do banco é realizada no [phpNyAdmin](https://localhost/phpmyadmin/). 

1. Crie um banco clicando em novo
2. Conectar o banco com o laravel, para isso acessamos o arquivo ``.ENV`` e colocamos os dados do nosso banco lá.

### Route
> Rota é um vinculo de uma url com uma função e precisa ter o método HTTP.

como exemplo:
```
Route::get('/', function () {
    return view('welcome');
});
```

Como vemos, primeiro é adicionado a uri e depois a função executada.

como exemplo:
```
Route::get('/aluno/{id}', function () {
    
});
```

#### Métodos HTTP

| Método | Descrição |
| --- | --- |
| `post` | insere/envia dado |
| `delete` | deleta/exclui dado |
| `put` | atualiza/altera um dado |
| `get` | lê dados |

### MVC

#### Controllers

O controller é o controlador da aplicação ele é primeiro a receber informação dentro da aplicação, com isso ele passa a informação para a model de for necessário o Banco de dados, ou com a View de for necessário somente apresentação de uma page.

o comando de criação do controller é:
```
php artisan make:controller classeController
```
O Controller é criado dentro de ``App/Http/controller``.

como no exemplo a seguir:

```
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class alunoController extends Controller
{
    public function addAluno(){
        
    }
}
```
A classe alunoController tratada no exemplo herda as propriedades de Controller, uma classe já pertencente ao Laravel .










