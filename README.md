# Desafio de Plugin WordPress: Sistema de Divulgação de Cursos

## Índice

- [Objetivo](#objetivo)
- [Requisitos Regras de Negócio](#requisitos-regras-de-negócio)
- [Requisitos Técnicos](#requisitos-técnicos)
- [Critérios de Avaliação](#critérios-de-avaliação)
- [Opções de Submissão](#opções-de-submissão)
- [Observações](#observações)

## Objetivo

Desenvolver um plugin WordPress para gerenciamento e divulgação de cursos,
demonstrando habilidades avançadas em desenvolvimento WordPress,
boas práticas de programação e capacidade de resolução de problemas complexos.

## Requisitos Regras de Negócio

1. Custom Post Type: Curso Fuerza
   - Campos padrão:
     - Título
     - Conteúdo
     - Imagem destacada
   - Campos adicionais:
     - Link de Inscrição (URL completa)
     - Carga Horária (Exemplo: 100 horas)
     - Data Limite de Inscrições (Apenas data, exemplo: DD/MM/YYYY)
     - Nível do Curso (Exemplo: Iniciante, Intermediário, Avançado)

2. Frontend
   - Exibição personalizada na single do curso:
     - Antes do conteúdo:
       - Carga Horária
         - Exemplo: 100 horas
       - Data Limite de Inscrições
          - Formato: DD/MM/YYYY
       - Nível do Curso
     - Após o conteúdo:
       - Se a Data Limite não tiver passado:
         - Exibir formulário "Tenho Interesse"
       - Se a Data Limite tiver passado:
         - Exibir apenas o Link de Inscrição
   - Formulário "Tenho Interesse":
     - Envio do formulário via WP REST API
     - Armazenamento em tabela personalizada com as seguintes colunas:
       - ID (auto-incrementado)
       - Nome
       - E-mail
       - ID do Curso
       - Data/Hora do Cadastro
     - Validação: Não permitir cadastro com e-mail já registrado para o mesmo curso
     - Feedback ao usuário:
       - Mensagem de sucesso após submissão bem-sucedida
       - Mensagem de erro em caso de falha (e-mail duplicado, erro de servidor, etc.)
     - Redirecionamento: Após submissão bem-sucedida, redirecionar para o Link de Inscrição do curso

3. Admin
   - Metabox na edição do curso: Listagem de interessados
     - Campos a serem exibidos:
       - Nome
       - E-mail
       - Data/Hora do Cadastro
   - Coluna adicional na listagem de cursos:
     - Número de interessados

## Requisitos Técnicos

- Compatibilidade: PHP 8.2+, WordPress 6.6+
  - Não pode aceitar ativação do plugin se não passar nos testes de compatibilidade
- Uso de Composer para autoloading (PSR-4)
- Aderência às PSR-1 e PSR-12
- Implementação de testes automatizados (PHPUnit ou outro framework de testes)
- Utilização correta das práticas de internacionalização (i18n) do WordPress
- README.md com instruções detalhadas para instalação, configuração e uso do plugin

## Critérios de Avaliação

1. Arquitetura do código e padrões de projeto utilizados
2. Segurança, validação e performance
3. Aderência às melhores práticas do WordPress, incluindo i18n
4. Código limpo e organizado
5. Design patterns (Repository, Service, Factory, etc.)
6. Princípios de SOLID
7. Qualidade e cobertura dos testes automatizados (Não obrigatório, mas recomendável)
8. Boas práticas de reutilização de código
9. Capacidade de resolução de problemas e implementação de soluções criativas

## Opções de Submissão

- Opção 1: Realize um fork do repositório e submeta seu código via Pull Request.
- Opção 2: Crie um novo repositório e defina-o como privado adicionando o usuário @fuerzastudio como um colaborador do seu repositório.

Essa conta do Github (@fuerzastudio) é usada apenas por nossos engenheiros para baixar e revisar seu código

## Observações

- Embora fazemos uso de IA no dia a dia para ajudar no desenvolvimento de soluções,
é altamente recomendável que você escreva o código baseado em boas práticas e conhecimentos que você já tem.

Boa Sorte! 🤞🏽
