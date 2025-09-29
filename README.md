# RotaBus

## Sobre o projeto

RotaBus é um sistema integrado para facilitar o transporte escolar e universitário em cidades do interior. Muitas cidades próximas a polos educacionais possuem estudantes que dependem de transporte coletivo para chegar até suas instituições, mas atualmente o processo de organização do transporte é manual, lento e pouco eficiente.

Nosso objetivo é automatizar todo esse processo por meio de um aplicativo mobile para os alunos e um sistema web para as prefeituras, onde:

- Os estudantes indicam se vão usar o transporte no dia, ida, volta ou ambos.
- O sistema gera automaticamente a melhor rota para o motorista, com base nos locais e confirmações.
- Antes de embarcar, o aluno escaneia um QR Code para confirmar presença no transporte.
- As prefeituras têm acesso a um dashboard completo com dados e relatórios do transporte.

## Problema atual

- Organizar rotas manualmente a partir de listas que os estudantes enviam diariamente.
- Dificuldade em confirmar presença real dos alunos no transporte.
- Falta de transparência e dados para a gestão das prefeituras.
- Alto custo e desperdício de recursos devido à má otimização das rotas.

<img src="https://github.com/user-attachments/assets/dd55f137-33c9-48b1-b075-7b8c8f6b347b" width="200" />
<img src="https://github.com/user-attachments/assets/9c499715-5716-47b1-bb10-a9ff26e514c7" width="200" />
<img src="https://github.com/user-attachments/assets/4bbb867a-2ff7-49c1-b720-9f96214a63cf" width="200" />

## Como o RotaBus resolve

- Automatização completa do cadastro e confirmação dos alunos.
- Geração dinâmica e inteligente de rotas via integração com APIs de mapas.
- Confirmação de presença via QR Code no embarque.
- Dashboard web para monitoramento e análise dos dados do transporte.

## Status do projeto

O projeto está em fase inicial. A equipe já definiu a arquitetura, tecnologias e está começando o desenvolvimento do backend e app mobile.

---

## Tecnologias planejadas

- Mobile: React Native
- Backend: Python (FastAPI)
- Banco de dados: PostgreSQL
- API de mapas: OpenRouteService + OpenStreetMap
- Autenticação: OAuth2 + JWT + RBAC
- Infraestrutura: CloudFlare Workers
- CI/CD: GitHub Actions
- Design UI/UX: Figma + Material UI

---

## Regras de Branch

### Estrutura de Branches

1. **`main`**  
   - Branch principal e protegida.  
   - Somente *merge commits* aprovados via Pull Request (PR) vindos de develop são aceitos aqui.  
   - Deve sempre refletir o código em produção.

2. **`develop`**  
   - Branch de integração onde todas as features são integradas antes do deploy.  
   - Recebe PRs das branches de feature.  
   - Pode ser atualizada diretamente apenas por membros da equipe com permissão.

3. **Branches de Feature**  
   - Sempre crie uma branch nova para cada feature, bugfix ou melhoria a partir da `develop`.  
   - Nomeie a branch no formato: `feature/nome-descritivo` ou `bugfix/nome-descritivo`.  
   - Exemplo: `feature/login-usuario`, `bugfix/corrigir-titulo`.

---

### Fluxo de Trabalho

1. Crie a branch de feature a partir da branch `develop`:

    ```bash
    git checkout develop
    git pull origin develop
    git checkout -b feature/nome-da-feature
    ```

2. Faça commits claros e atômicos dentro da sua branch de feature.

3. Antes de enviar o PR, mantenha sua branch atualizada com a `develop`:

    ```bash
    git checkout develop
    git pull origin develop
    git checkout feature/nome-da-feature
    git rebase develop
    ```

4. Abra um Pull Request da sua branch de feature para a branch `develop`.  
   - Descreva bem o que foi feito.  
   - Marque revisores e aguarde aprovação.

5. Após aprovação, faça o merge do PR na branch `develop`.

6. Periodicamente, será integrado `develop` na `main` através de PRs, sempre respeitando a política de revisão e proteção.

---

### Regras de Commit

- Use mensagens de commit claras e padronizadas, preferencialmente seguindo um padrão, como o [Conventional Commits](https://www.conventionalcommits.org/pt-br/). Exemplo:  
  - `feat: adicionar funcionalidade de login`  
  - `fix: corrigir erro na validação do formulário`  
  - `docs: atualizar README com instruções de setup`
  - `style: mudanças visuais`

- Evite commits muito grandes; prefira commits pequenos que representem etapas lógicas.

---

## Desenvolvido por

**SixBro Corporation**

- [@franklin-samuel](https://github.com/franklin-samuel)  
- [@pedrohenrc](https://github.com/pedrohenrc)  
- [@pedroromulo3](https://github.com/pedroromulo3)  
- [@PedroHeitor12567](https://github.com/PedroHeitor12567)  
- [@Wallysom-fer](https://github.com/Wallysom-fer) 
- [@Pedro-Carvalhodev](https://github.com/Pedro-Carvalhodev)

## Contato

SixBro Corporation - samuelfranklinff@gmail.com - (84) 9 9921-6842


