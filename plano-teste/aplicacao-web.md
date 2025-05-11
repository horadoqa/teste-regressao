# ✅ **Plano de Teste de Regressão – Aplicação Web**

## 1. **Objetivo**

Assegurar que funcionalidades existentes da aplicação web continuam funcionando corretamente após modificações no código-fonte (correções, melhorias ou novas funcionalidades), evitando efeitos colaterais inesperados.

---

## 2. **Escopo**

### Inclui:

* Funcionalidades principais da aplicação (autenticação, navegação, formulários, buscas, etc.)
* Interface do usuário (UI)
* Integrações com APIs e serviços externos
* Fluxos críticos de negócio

### Não Inclui:

* Funcionalidades ainda em desenvolvimento
* Testes exploratórios ou de usabilidade
* Testes de segurança profunda (a menos que parte do escopo do sprint)

---

## 3. **Critérios de Entrada**

* Ambiente de testes configurado e estável
* Versão do sistema implantada no ambiente de QA/homologação
* Casos de teste documentados ou scripts automatizados prontos
* Acesso garantido aos recursos necessários (dados de teste, contas, tokens)

---

## 4. **Critérios de Saída**

* Todos os testes planejados foram executados
* Nenhuma falha crítica em funcionalidades existentes
* Relatório de execução e defeitos documentado
* Aprovação do time de QA (ou líder de testes)

---

## 5. **Tipos de Testes Envolvidos**

* Testes funcionais manuais
* Testes automatizados (UI e API)
* Testes de performance (opcional, com K6 ou JMeter)
* Testes de compatibilidade entre navegadores

---

## 6. **Ferramentas**

* **Automação:** Selenium, Cypress, Playwright, Puppeteer
* **Testes de API:** Postman, REST-assured
* **Testes de carga:** K6
* **Gerenciamento de testes:** TestRail, Zephyr, Xray ou planilhas
* **CI/CD:** Jenkins, GitHub Actions, GitLab CI

---

## 7. **Responsabilidades**

| Papel                     | Responsável    |
| ------------------------- | -------------- |
| Analista de QA            | Fulano de Tal  |
| Desenvolvedor responsável | Ciclano de Tal |
| Gerente de Qualidade      | Beltrano       |

---

## 8. **Matriz de Casos de Teste Regressivos (Exemplos)**

| ID    | Funcionalidade          | Caso de Teste                           | Prioridade | Autom. | Status   |
| ----- | ----------------------- | --------------------------------------- | ---------- | ------ | -------- |
| TC001 | Login                   | Verificar login com credenciais válidas | Alta       | Sim    | Passou   |
| TC002 | Login                   | Erro ao tentar logar com senha errada   | Alta       | Sim    | Passou   |
| TC003 | Cadastro de usuário     | Criar novo usuário com dados válidos    | Alta       | Não    | Falhou   |
| TC004 | Página de produtos      | Verificar listagem e filtro             | Média      | Sim    | Passou   |
| TC005 | Carrinho de compras     | Adicionar e remover itens               | Alta       | Sim    | Passou   |
| TC006 | Responsividade (mobile) | Visualização em smartphone              | Baixa      | Não    | Pendente |

---

## 9. **Cronograma Estimado**

| Atividade               | Tempo estimado  |
| ----------------------- | --------------- |
| Preparação de ambiente  | 1 dia           |
| Execução dos testes     | 1–3 dias        |
| Análise e relatório     | 0,5 dia         |
| Correções e revalidação | Conforme falhas |

---

## 10. **Riscos e Mitigações**

| Risco                                   | Ação de Mitigação                        |
| --------------------------------------- | ---------------------------------------- |
| Ambiente instável                       | Garantir monitoramento e backups diários |
| Dados inconsistentes nos testes         | Criar massa de dados controlada          |
| Mudanças de última hora no código       | Congelamento de release antes do teste   |
| Baixa cobertura de testes automatizados | Priorização de testes manuais críticos   |

---

## 11. **Critérios de Sucesso**

* 100% dos casos críticos executados e aprovados
* Falhas médias e baixas documentadas e com plano de correção
* Relatório final aprovado pela liderança de QA/Desenvolvimento

---

