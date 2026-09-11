# Connecta

Aplicação web progressiva (PWA) para gestão de equipes, comunicação interna e gamificação organizacional.

🔗 **Demo ao vivo:** https://connecta.sbs/

---

## Sobre o projeto

O Connecta centraliza a operação de uma equipe em uma única plataforma: cadastro e organização de pessoas, comunicação interna, controle de permissões por perfil e mecânicas de gamificação para elevar o engajamento do time.

O projeto foi construído de ponta a ponta — modelagem de dados, autenticação, regras de autorização no cliente e no servidor, e publicação em produção.

## Funcionalidades

- Autenticação de usuários com Firebase Authentication
- Controle de acesso por perfis (Admin / Usuário)
- CRUD completo dos registros da plataforma
- Comunicação interna entre membros da equipe
- Gamificação aplicada ao engajamento organizacional
- Deploy automatizado

## Stack

| Camada | Tecnologia |
| --- | --- |
| Front-end | JavaScript (Vanilla), HTML5, CSS3 |
| Autenticação | Firebase Authentication |
| Banco de dados | Cloud Firestore (NoSQL) |
| Entrega | PWA + pipeline de deploy automatizado |

## Arquitetura

Aplicação SPA construída sem framework, consumindo o SDK do Firebase diretamente. A autorização é resolvida no cliente por perfil de usuário, enquanto as regras de segurança do Firestore fazem a proteção real dos dados no servidor.

## Como executar localmente

1. Clone o repositório:
   `git clone https://github.com/pedroqueirozbatera-alt/connecta.git`
2. Configure suas credenciais do Firebase no arquivo de configuração do projeto
3. Sirva a pasta com um servidor local (ex.: Live Server do VS Code)
4. Acesse `http://localhost:5500` no navegador

## Segurança

As regras do Firestore são a camada real de proteção dos dados.

- Nunca versione o arquivo de service account (`*firebase-adminsdk*.json`)
- Mantenha no `.gitignore`: `node_modules/`, `dist/` e o JSON da service account

O `firebaseConfig` do front-end pode ser público sem risco — quem protege os dados são as regras do Firestore.

## Autor

**Pedro Henrique Corrêa de Queiroz** — Brasília/DF

- LinkedIn: https://www.linkedin.com/in/pedro-henrique-queiroz-610673399/
- GitHub: https://github.com/pedroqueirozbatera-alt
