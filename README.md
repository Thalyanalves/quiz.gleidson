## 🚀 README do Projeto "Quiz Front-Web"

Este projeto consiste em um Quiz simples de desenvolvimento Front-End (HTML, CSS e JavaScript) implementado com três arquivos principais: `index.html`, `quiz.html`, `score.html` e o *script* `script.js`, além dos arquivos de estilo e imagem de fundo.

---

### 1. ⚙️ Estrutura do Projeto

O projeto segue a seguinte organização de arquivos:

* **`index.html`**: A página inicial do quiz.
* **`quiz.html`**: A página onde as perguntas são exibidas.
* **`score.html`**: A página que exibe a pontuação final.
* **`script.js`**: O arquivo principal com a lógica do quiz (perguntas, respostas e pontuação).
* **`styles.css`**: Arquivo de estilos CSS para a aparência do quiz.
* **`Images/4850268.jpg`**: Imagem de fundo utilizada nas páginas.

---

### 2. 📝 Descrição das Páginas

#### **2.1. `index.html` (Página Inicial)**

* [cite_start]**Título:** "Bem-vindo ao Quiz Front-Web!" [cite: 2]
* [cite_start]**Descrição:** "Teste seus conhecimentos em desenvolvimento web." [cite: 3]
* **Ações:** Possui dois botões:
    * [cite_start]**"Iniciar Quiz"**: Inicia o quiz redirecionando o usuário para `quiz.html` e chamando a função `IniciarQuiz()` do JavaScript, que carrega a primeira pergunta. [cite: 4]
    * [cite_start]**"Score"**: Redireciona o usuário para `score.html` para visualizar a pontuação mais recente. [cite: 5]

#### **2.2. `quiz.html` (Página do Quiz)**

* **Estrutura:** Exibe a pergunta e duas opções de resposta (Verdadeiro ou Falso).
* [cite_start]**Interação:** As opções de **"Verdadeiro"** e **"Falso"** são elementos clicáveis (`onclick="certo()"`) e ativam a função de verificação da resposta e avanço para a próxima pergunta (`quiz()`). [cite: 55, 56, 53]
* [cite_start]**Navegação:** Possui um botão **"Home"** para retornar à página inicial. [cite: 57]
* **Exemplos de Perguntas:**
    * [cite_start]"A tag **head** é usada para incluir metadados sobre o documento, como o conjunto de caracteres e o título da página, e não é exibida no corpo principal da página?" [cite: 19, 102]
    * [cite_start]"Para alterar a **cor de fundo (background)** de um elemento HTML, a propriedade **color** deve ser utilizada?" [cite: 54, 137]
    * [cite_start]"Em **JavaScript**, **strings** é o tipo de dado fundamental usado para representar texto, e é delimitado por aspas simples." [cite: 71, 72, 154, 155]

#### **2.3. `score.html` (Página de Pontuação)**

* [cite_start]**Exibição:** Mostra o título **"Sua Pontuação"** [cite: 36] [cite_start]e a pontuação final salva no **`localStorage`** pelo *script*. [cite: 37]
* [cite_start]**Navegação:** Possui um botão **"Home"** para retornar à página inicial. [cite: 38]

---

### 3. 🧠 Lógica do Quiz (`script.js`)

O arquivo `script.js` contém toda a lógica do quiz:

* **Estrutura de Perguntas e Respostas:**
    * As perguntas estão armazenadas em um *array* chamado `numero` (índices 1 a 20).
    * As respostas corretas (onde **1** = Verdadeiro, **0** = Falso) estão em um *array* chamado `resultado`.
    * Exemplo de Mapeamento:
        * `numero[2] = 'Para alterar a cor de fundo (background) de um elemento HTML, a propriedade color deve ser utilizada?';`
        * `resultado[2] = 0;` (Falso, pois a propriedade correta é `background-color`).
* **Funções Principais:**
    * `IniciarQuiz()`: Redireciona o navegador para `quiz.html`.
    * `quiz()`: Exibe a pergunta atual. Se o índice (`i`) for maior que 20, **salva a pontuação** (`score`) no `localStorage` sob a chave **`finalQuizScore`** e redireciona para `score.html`.
    * `certo()` / `errado()`: Chamadas ao clicar nas opções. Elas verificam se a resposta do usuário (1 ou 0) corresponde ao valor em `resultado[i]`.
        * **Acerto:** Incrementa a variável **`score`** e muda a cor de fundo da opção para verde (`#69e36fff`).
        * **Erro:** Muda a cor de fundo da opção selecionada para vermelho (`#DC143C`).
        * Em seguida, incrementam o índice da pergunta (`i++`) e chamam `quiz()` para a próxima pergunta.
    * `Colors()`: Função de *mouseover* que limpa a cor de fundo das opções.
* **Mecanismo de Pontuação e Redirecionamento:**
    * A pontuação é mantida na variável global `score`.
    * Ao final do quiz (`i > 20`), a pontuação final é armazenada no **`localStorage`** antes de o usuário ser enviado para `score.html`.
    * Em `score.html`, o script recupera o valor de `localStorage.getItem('finalQuizScore')` e o exibe.

---

### 4. 🎨 Estilização (`styles.css`)

* O estilo define um fundo com imagem (`background-image:url(Images/4850268.jpg)`) e uma paleta de cores primária em tons de roxo/azul. * As perguntas são exibidas em um fundo azul claro (`#c7dde6`) e as opções em branco (`#ffffff`).
* As interações de *hover* e clique fornecem *feedback* visual, mudando o fundo das opções.
* [cite_start]O *layout* é centralizado, com largura máxima de **1000px** [cite: 1472] para melhor visualização em telas maiores.

---

### 5. 🧑‍🤝‍🧑 Integrantes

O projeto foi desenvolvido por:

* [cite_start]Daniel Nascimento [cite: 82]
* [cite_start]Kayla Magalhães [cite: 83]
* [cite_start]Thalyana Mendes [cite: 83]
