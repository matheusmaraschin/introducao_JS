# Checkpoint — pause e responda

### 1. Em qual aba das ferramentas do desenvolvedor a mensagem apareceu?

**R:** A mensagem apareceu na aba de console.

### 2. O atributo `defer` faz o navegador esperar o HTML ser lido antes de executar o script. Por que isso será importante mais adiante, quando o script precisar mexer em elementos da página?

**R:** Pois isso garante que o HTML seja completamente carregado antes do JavaScript.

### 3. Se você escrevesse `<script src="codigo.js" defer>` no HTML, mas o arquivo se chamasse `script.js`, o que aconteceria?

**R:** Dá erro, pois o HTML não encontra o arquivo:

```text
Refused to execute script from 'http://127.0.0.1:5500/codigo.js'
because its MIME type ('text/html') is not executable,
and strict MIME type checking is enabled.
```

---

# Checkpoint — pause e responda

### 1. Por que `"5" + 3` e `"5" - 3` dão resultados tão diferentes?

**R:** Pois o operador `+` faz concatenação de strings, mesmo se só um termo estiver em string. Já o operador `-` serve apenas para operações matemáticas, então ele converte a string `"5"` em número.

### 2. Por que `2 + 3 * 4` e `(2 + 3) * 4` dão resultados diferentes?

**R:** Pois, na matemática, os parênteses têm prioridade e devem ser resolvidos primeiro.

---

# Checkpoint — pause e responda

### 1. Antes de executar, escreva o que as quatro linhas com `typeof` vão imprimir:

**R:**

```text
string
number
boolean
undefined
```

### 2. Qual erro apareceu no console na última linha? Por que ele ocorre?

**R:**

```text
script.js:12 Uncaught TypeError: Assignment to constant variable.
    at script.js:12:8
```

Ele ocorre porque a variável `escola` é declarada com `const`, ou seja, não pode ser reatribuída.

### 3. Quais destes nomes de variável são válidos? Marque e justifique os inválidos.

- [x] `nota_final`
- [ ] `3nota`
- [ ] `nota-final`
- [x] `$total`
- [ ] `class`

**R:** `nota_final` e `$total` são válidos. Não pode começar com número, não pode ter hífen e não pode utilizar palavras reservadas da linguagem.

### 4. Observe o código abaixo e diga o que será impresso. Depois confira no console.

```javascript
let idade = 15;

idade = idade + 1;

console.log(idade);
```

**R:** `16`

---

# Checkpoint — pause e responda

### 1. Escreva a saída prevista de cada `console.log` (são 8 linhas de saída). Depois execute e corrija o que errou.

**R:**

```text
script.js:9 5 14
script.js:4 3.5
script.js:5 1
script.js:6 49
script.js:8 Olá, Ana! 7 dividido por 2 é 3.5
script.js:10 8.5
script.js:11 7.51
script.js:12 NaN
```

### 2. Qual é a diferença entre `Number("7.5") + 1` e `"7.5" + 1`? O que isso significa para quem lê um número digitado em um campo de formulário?

**R:** `Number("7.5")` transforma o texto em um número e soma `+1`. Já `"7.5" + 1` faz concatenação, juntando o número ao texto.

### 3. Sem executar, calcule: `10 % 3`, `2 ** 3` e `10 / 4`. Depois confira no console.

**R:** `1`, `8` e `2.5`.

---

# Checkpoint — pause e responda

### 1. Com `temperatura = 20`, qual mensagem aparece? E com `30`? Por quê?

**R:** Agradável e Calor. Pois esses são os valores definidos pelos testes de condição.

### 2. Quais as saídas das quatro últimas linhas? Por que recomendamos `===`?

**R:**

```text
script.js:11 true
script.js:12 false
script.js:13 true
script.js:14 false
```

O operador `==` tenta converter os valores para o mesmo tipo antes de comparar. Já o operador `===` compara os valores e também os tipos, sem fazer conversão automática.

### 3. Escreva uma condição que seja verdadeira apenas quando a variável `nota` estiver entre 0 e 10 (inclusive):

**R:**

```javascript
let nota = 8.5;

if (nota >= 0 && nota <= 10) {
    console.log("Nota válida!");
} else {
    console.log("Nota inválida! Digite um valor entre 0 e 10.");
}
```