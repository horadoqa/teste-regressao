# ✅ **Plano de Teste de Regressão para uma Página Web**

## 1. **Objetivo**

Garantir que as funcionalidades existentes da página web continuem funcionando corretamente após modificações no código (como correções de bugs, atualizações ou novas funcionalidades).

## 2. **Escopo**

Testar as principais funcionalidades da página web, incluindo:

* Carregamento da página
* Elementos visuais (botões, links, imagens)
* Funcionalidades interativas (formulários, filtros, etc.)
* Integrações com serviços externos (APIs, autenticação)
* Compatibilidade entre navegadores (se aplicável)

## 3. **Critérios de Entrada**

* Código atualizado implantado em ambiente de testes
* Ambiente estável e funcional
* Casos de teste existentes ou identificados
* Scripts automatizados (se houver) atualizados

## 4. **Critérios de Saída**

* Todos os testes regressivos executados
* Nenhuma falha crítica em funcionalidades existentes
* Relatório de execução de testes gerado e validado

## 5. **Responsabilidades**

| Papel              | Responsável            |
| ------------------ | ---------------------- |
| Analista de Testes | \[Nome do responsável] |
| Desenvolvedor      | \[Nome do responsável] |
| Gerente de QA      | \[Nome do responsável] |

## 6. **Ferramentas Utilizadas**

* Automação: Selenium, Cypress, Playwright (opcional)
* Teste de performance: K6 (caso necessário)
* Gerenciamento de testes: TestRail, Zephyr, ou Excel/Planilhas
* CI/CD: Jenkins, GitHub Actions, GitLab CI, etc.

## 7. **Casos de Teste Regressivos (Exemplos)**

| ID   | Funcionalidade          | Descrição                                             | Resultado Esperado                             |
| ---- | ----------------------- | ----------------------------------------------------- | ---------------------------------------------- |
| TC01 | Carregamento da Home    | Verificar se a página inicial carrega corretamente    | Página carrega com todos os elementos visíveis |
| TC02 | Navegação entre páginas | Testar cliques em links de navegação                  | Usuário é redirecionado corretamente           |
| TC03 | Validação de formulário | Submissão de formulário com dados válidos e inválidos | Comportamento esperado para cada cenário       |
| TC04 | Responsividade          | Verificar exibição em diferentes tamanhos de tela     | Layout ajusta corretamente                     |
| TC05 | Desempenho (com K6)     | Avaliar tempo de resposta do backend                  | Dentro dos limites definidos (< 500ms, etc)    |

## 8. **Riscos**

* Mudanças de última hora no código
* Dados inconsistentes no ambiente de testes
* Falta de cobertura de testes automatizados

## 9. **Cronograma Estimado**

| Etapa                  | Duração Estimada |
| ---------------------- | ---------------- |
| Planejamento           | 0.5 dia          |
| Preparação de ambiente | 0.5 dia          |
| Execução dos testes    | 1 a 2 dias       |
| Análise e relatório    | 0.5 dia          |

## 10. **Critérios de Sucesso**

* 100% dos testes críticos aprovados
* Sem regressões funcionais ou de performance
* Feedback positivo da equipe de QA e desenvolvedores

---

