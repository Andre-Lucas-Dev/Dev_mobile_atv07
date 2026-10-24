# Cadastro de Usuário

Aplicativo Flutter com uma tela de cadastro de usuário, desenvolvido como atividade prática. A tela captura os dados digitados, aplica filtros de entrada, valida cada campo e dá feedback visual ao usuário.

## Resultado final

<img width="447" height="895" alt="image" src="https://github.com/user-attachments/assets/a9c5f84b-09bd-4294-bf6e-8738683dd41b" />


![Print do app funcionando](COLE_AQUI_O_LINK_DA_IMAGEM)

## Funcionalidades

- Formulário com `Form`, `TextFormField` e `GlobalKey<FormState>`
- Campos: nome completo, e-mail, CPF, telefone, senha e confirmação de senha
- `keyboardType` e `inputFormatters` adequados a cada campo (CPF e telefone aceitam somente números)
- Validação campo a campo, com mensagens de erro exibidas abaixo de cada campo inválido
- `SnackBar` verde de sucesso quando o cadastro é válido
- `SnackBar` vermelho de erro quando há campos inválidos
- Botão para mostrar/ocultar a senha
- Validação de e-mail com `RegExp`
- Confirmação de senha, verificando se os dois valores são iguais

## Regras de validação

| Campo | Regra |
|---|---|
| Nome completo | Obrigatório |
| E-mail | Obrigatório, deve conter `@` e ter formato válido |
| CPF | Obrigatório, somente números, 11 dígitos |
| Telefone | Obrigatório, somente números, 10 ou 11 dígitos |
| Senha | Obrigatória, mínimo de 6 caracteres |
| Confirmar senha | Obrigatória, deve ser igual à senha |

## Estrutura da tela

```
Scaffold
└── Form(key: _formKey)
    └── SingleChildScrollView
        └── Column
            ├── TextFormField (nome)
            ├── TextFormField (e-mail)
            ├── TextFormField (CPF)
            ├── TextFormField (telefone)
            ├── TextFormField (senha)
            ├── TextFormField (confirmar senha)
            └── ElevatedButton (CADASTRAR)
