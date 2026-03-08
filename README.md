# Teste Técnico QA – 4blue

Este repositório contém a documentação do **teste técnico de QA** realizado como parte do processo seletivo da **4blue**.

Aqui estão registrados o plano de testes, as sessões de testes exploratórios realizadas e os defeitos encontrados durante a avaliação da aplicação.

---

# Estrutura do Projeto

A documentação foi organizada da seguinte forma:

## Plano de Testes

Define o escopo do teste, as funcionalidades avaliadas e as condições de teste planejadas.

-  [Plano de Testes](https://github.com/celiapaivab/teste-tecnico-4blue/wiki/Plano%E2%80%90de%E2%80%90Testes)

---

## Missões de Teste

As sessões de **testes exploratórios** foram divididas em três missões:

-  [Missão 01 – Testes Visuais](https://github.com/celiapaivab/teste-tecnico-4blue/wiki/Missao%E2%80%9001%E2%80%90Testes%E2%80%90Visuais)

-  [Missão 02 – Cadastro](https://github.com/celiapaivab/teste-tecnico-4blue/wiki/Missao%E2%80%9002%E2%80%90Cadastro)

-  [Missão 03 – Login](https://github.com/celiapaivab/teste-tecnico-4blue/wiki/Missao%E2%80%9003%E2%80%90Login)

Cada missão documenta:

- charter de teste  
- condições exploradas  
- observações da sessão  
- defeitos encontrados  
- perguntas levantadas durante o teste  

---

# Defeitos Encontrados

Os defeitos identificados durante os testes foram registrados como **Issues do GitHub**, simulando um fluxo real de gestão de bugs.

| ID | Título | Severidade | Prioridade |
|----|----|----|----|
| [BUG-01](https://github.com/celiapaivab/teste-tecnico-4blue/issues/1) | Inputs ultrapassam o limite da div do formulário na tela de cadastro | Baixo | Baixa |
| [BUG-02](https://github.com/celiapaivab/teste-tecnico-4blue/issues/2) | Sistema permite criação de conta com todos os campos vazios | Alto | Alta |
| [BUG-03](https://github.com/celiapaivab/teste-tecnico-4blue/issues/3) | Sistema permite cadastro com nome inválido | Médio | Média |
| [BUG-04](https://github.com/celiapaivab/teste-tecnico-4blue/issues/4) | Sistema permite cadastro com telefone inválido | Médio | Média |
| [BUG-05](https://github.com/celiapaivab/teste-tecnico-4blue/issues/5) | Sistema permite cadastro com email inválido ou vazio | Alto | Alta |
| [BUG-06](https://github.com/celiapaivab/teste-tecnico-4blue/issues/6) | Sistema permite cadastro com senha que não atende às regras definidas | Alto | Alta |
| [BUG-07](https://github.com/celiapaivab/teste-tecnico-4blue/issues/7) | Sistema permite cadastro quando senha e confirmação são diferentes | Alto | Alta |
| [BUG-08](https://github.com/celiapaivab/teste-tecnico-4blue/issues/8) | Sistema exibe mensagem de erro inesperado após login com credenciais válidas | Médio | Média |
| [BUG-09](https://github.com/celiapaivab/teste-tecnico-4blue/issues/9) | Sistema permite login com dados inválidos ou campos vazios | Crítico | Alta |

---

# Estratégia de Teste

Os testes foram conduzidos utilizando **testes exploratórios baseados em sessões**, com foco nas seguintes funcionalidades:

- Interface e layout da aplicação  
- Criação de conta  
- Autenticação de usuários  

A abordagem exploratória permitiu identificar problemas relacionados a:

- validação de campos  
- comportamento da interface  
- inconsistências de autenticação  

Não foi realizada verificação detalhada de **regras de negócio**, pois não foi disponibilizada documentação funcional ou especificação contendo essas regras durante a execução do teste.

---

# Priorização de Correção de Bugs

## 1. BUG-09 – Sistema permite login com dados inválidos ou campos vazios

Este bug foi priorizado por possuir **severidade crítica**, pois o sistema permite que o processo de autenticação seja concluído mesmo quando são informados dados inválidos ou campos vazios, indicando a ausência de validação adequada no login. Isso pode permitir que usuários acessem o sistema sem possuir credenciais válidas, o que compromete a segurança da aplicação. Além disso, diminui a confiabilidade do sistema e prejudica a experiência do usuário.

Por afetar uma funcionalidade central do sistema (login), este defeito deve ser tratado com **alta prioridade**.

---

## 2. BUG-02 – Sistema permite criação de conta com todos os campos vazios

Este bug foi priorizado por possuir **severidade alta** e impactar diretamente a integridade dos dados armazenados no sistema. Durante os testes, foi possível criar uma conta mesmo deixando todos os campos do formulário de cadastro vazios, o que indica ausência de validação obrigatória nos campos. Isso o pode gerar diversos problemas, como a criação de registros inválidos ou incompletos na base de dados, dificuldade na identificação de usuários e aumento de dados inconsistentes no sistema, podendo inclusive gerar sobrecargas desnecessárias. Além disso, falhas no processo de cadastro podem afetar diretamente funcionalidades posteriores, como login.

Por impactar diretamente a qualidade e consistência dos dados da aplicação, este defeito deve ser tratado com **alta prioridade**.

---

# Sugestões de Melhoria

Algumas melhorias que poderiam aumentar a qualidade e usabilidade das telas avaliadas:

- Implementar validação de campos no frontend e backend.
- Utilizar validação automática para o campo telefone.
- Implementar feedback visual imediato nos campos inválidos durante o preenchimento do formulário.
- Adicionar mensagens de erro claras e específicas para cada tipo de validação, evitando mensagens genéricas como "erro inesperado".


---

# Autor

**Celia Bruno**  - [LinkedIn](https://www.linkedin.com/in/celia-bruno/)
