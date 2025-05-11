# Teste de Regressão

O **teste de regressão** é um tipo de teste de software usado para verificar se mudanças recentes no código (como correções de bugs, adição de novas funcionalidades ou melhorias de desempenho) **não introduziram novos erros** ou **quebraram funcionalidades existentes**.

### Em outras palavras:

Quando você modifica o código de um sistema, há sempre o risco de que essa modificação afete partes que antes funcionavam corretamente. O teste de regressão garante que o software **ainda se comporta como esperado** após essas mudanças.

### Exemplos comuns:

* Após corrigir um bug no sistema de login, executa-se o teste de regressão para garantir que o cadastro de usuários, a recuperação de senha e outras funções relacionadas ainda funcionam.
* Depois de atualizar a biblioteca usada para gerar relatórios, verifica-se se todos os relatórios anteriores ainda são gerados corretamente.

### Como é feito?

* Pode ser feito manualmente, mas geralmente é **automatizado** (usando ferramentas como JUnit, Selenium, Cypress etc.).
* Envolve a **reexecução dos testes anteriores** (testes unitários, de integração, de interface etc.).

### Benefícios:

* Ajuda a evitar **efeitos colaterais indesejados**.
* Garante **estabilidade e confiabilidade** do sistema após mudanças.

### Exemplo:

Você **pode usar o K6 para realizar testes de regressão focados em performance** — e isso é uma excelente prática!

O K6 é uma ferramenta de **teste de carga e desempenho** (load testing), e embora o termo "teste de regressão" seja mais comum para testes funcionais, **regressões de performance** (quedas de desempenho após uma mudança) também são regressões — e o K6 é perfeito para detectá-las.

### Como usar o K6 para testes de regressão de performance:

1. **Crie um teste de base ("baseline")**:

   * Antes de qualquer mudança no código, você roda um teste de performance e salva os principais resultados (tempo de resposta, throughput, taxa de erros etc.).

2. **Rode o mesmo teste após a modificação**:

   * Após mudar o código, você executa o mesmo script com o K6 e **compara os resultados com o baseline**.

3. **Compare os resultados automaticamente ou manualmente**:

   * Pode usar ferramentas como Grafana + InfluxDB ou Prometheus para monitorar e visualizar diferenças.
   * Ou salvar os resultados como JSON/CSV e comparar com scripts personalizados.

---

### Exemplo básico de script com K6:

```js
import http from 'k6/http';
import { check, sleep } from 'k6';

export let options = {
  vus: 50,
  duration: '5m',
};

export default function () {
  let res = http.get('https://sua-api.com/endpoint');
  
  check(res, {
    'status é 200': (r) => r.status === 200,
    'tempo de resposta < 500ms': (r) => r.timings.duration < 500,
  });

  sleep(1);
}
```

### Executando:

```bash
k6 run teste.js
```

Depois da modificação no código, rode o mesmo script e compare métricas como:

* `http_req_duration`
* `http_req_failed`
* `vus`, `iterations`
* `latency`, `throughput`

---

