# Desafio Back-end PicPay

Primeiramente, obrigado pelo seu interesse em trabalhar na melhor plataforma de pagamentos do mundo!
Abaixo você encontrará todos as informações necessárias para iniciar o seu teste.

## Avisos antes de começar

- Primeiro crie uma branch a partir da `master` nesse padrão de nomenclatura: dd-mm-yy/nome-sobrenome (por exemplo, 30-04-20/meu-nome)
- Você poderá consultar o Google, Stackoverflow ou algum projeto particular na sua máquina.
- Fique à vontade para perguntar qualquer dúvida aos recrutadores.
- Fique tranquilo, respire, assim como você, também já passamos por essa etapa. Boa sorte! :)

## Setup do projeto

- Laravel 5.8
- PHP > 7.2

## Como Rodar?

### Local

- Instale as dependências usando o comando `composer install`
- Na raiz do repositório, rode este comando `php artisan serve` para iniciar o servidor de desenvolvimento.
- A Aplicação estará disponível na porta `http://localhost:8000/`

### Docker
- Instale o Docker
- Execute `docker-compose up -d`
- A Aplicação estará disponível na porta `http://localhost:8000/`

## Objetivo - PicPay Simplificado

Tem-se **usuários comuns** e **lojistas**, ambos têm carteira com dinheiro. **Usuários comuns** podem enviar dinheiro (efetuar transações) para lojistas e entre **usuários comuns**. 

- Serviço autorizador deve ser externo, use este mock (https://run.mocky.io/v3/8fafdd68-a090-496f-8c9a-3442cf30dae6).

- Lojistas não podem enviar dinheiro para usuários. 

- Deve verificar se o usuário tem saldo suficiente

- A operação de transferência deve ser uma transação (ou seja, revertida em qualquer caso de inconsistência) e o dinheiro deve voltar para a carteira do usuário que envia. 

- Esse serviço funciona via interface RESTful. 

![image](https://user-images.githubusercontent.com/18670067/84683252-5264e100-af0d-11ea-927f-fec30fc26ffa.png)


### Payload

POST /transaction

```json
{
    "value" : 100.00,
    "payer" : 4,
    "payee" : 15
}
```
Retorno
```json
{
    "value" : 100.00,
    "payer" : 4,
    "payee" : 15,
    "transaction_date": "06/10/2020 20:00:00"
}
```


## O que será avaliado
- Uso de features do framework
- Modelagem de Dados
- Domínio da Linguagem
- Legibilidade do Código
- Estrutura do Código
- Organização do Código
- Manutenibilidade do Código
- Tratamento de erros

## O que será um diferencial
- Criação de imagem própria (Dockerfile)
- Testes de integração
- Uso de Design Patters
- No recebimento de pagamento, o usuário ou lojista precisa receber notificação enviada por um serviço de terceiro e eventualmente pode estar indisponível (https://run.mocky.io/v3/b19f7b9f-9cbf-4fc6-ad22-dc30601aec04). 

## Para o dia da avaliação
Na data marcada pelo recrutador tenha sua aplicacao rodando na sua máquina local.

## Documentação Laravel

https://laravel.com/docs

## Sugestões de estudo

- https://laracasts.com

- https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing

