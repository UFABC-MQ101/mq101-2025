# MQ101 — Guia de Submissão de Exercícios (2025)

Este guia descreve como enviar suas listas de exercícios no repositório público do curso:
https://github.com/UFABC-MQ101/mq101-2025

O fluxo padrão é: **fork → clone → branch → commit → push → Pull Request**.

---

## 0. Pré-requisitos mínimos

1. Conta no GitHub.
2. Git instalado no computador.
3. R (e RStudio/Posit) instalado.
4. (Recomendado) Quarto instalado para renderizar HTML/PDF a partir de `.qmd`/`.Rmd`.

---

## 1. Estrutura obrigatória da submissão

Para cada exercício `ex01`, crie exatamente esta estrutura:

```

exercises/submissions/ex01/<RA>-<sobrenome>/
├─ README.md
├─ script.R                 (obrigatório)
├─ respostas.Rmd ou respostas.qmd (recomendado, se aplicável)
├─ respostas.html OU respostas.pdf OU respostas.docx (obrigatório)
└─ (opcional) figures/ e output/

````

Regras:
- Use **um diretório por exercício**.
- Não altere arquivos de outras pessoas.
- Não inclua dados pessoais sensíveis.
- Evite arquivos grandes sem necessidade.

---

## 2. Fluxo recomendado (fork → clone → branch → commit → push → PR)

### 2.1. Faça um fork do repositório do curso
1. Acesse: https://github.com/UFABC-MQ101/mq101-2025
2. Clique em **Fork** (canto superior direito).
3. Confirme para criar seu fork na sua conta.

### 2.2. Clone o seu fork para o computador
No terminal:

```bash
git clone https://github.com/<seu-usuario>/mq101-2025.git
cd mq101-2025
````

### 2.3. Crie uma branch para o exercício

Nunca trabalhe direto na `main`:

```bash
git checkout -b ex01-<RA>-<sobrenome>
```

Exemplo:

```bash
git checkout -b ex01-123456-silva
```

---

## 3. Crie a pasta da sua submissão

Crie a pasta seguindo o padrão:

```bash
mkdir -p exercises/submissions/ex01/<RA>-<sobrenome>
```

No Windows PowerShell, se necessário:

```powershell
New-Item -ItemType Directory -Path exercises\submissions\ex01\<RA>-<sobrenome>
```

---

## 4. Reprodutibilidade (exigências)

### 4.1. `script.R` (obrigatório)

O `script.R` deve rodar “do zero”. Requisitos:

* Usar **caminhos relativos** (nunca `C:\Users\...`).
* Carregar pacotes explicitamente (`library(...)`).
* Incluir `set.seed()` quando houver simulação.
* Incluir `sessionInfo()` no final.

Cabeçalho recomendado:

```r
# MQ101 — Exercício 01
# Nome: <Seu nome completo>
# RA: <Seu RA>
# Data: <YYYY-MM-DD>
# Como reproduzir:
# 1) abrir o projeto no RStudio
# 2) rodar este script do início ao fim
```

No final do script:

```r
sessionInfo()
```

### 4.2. Relatório em `.Rmd` ou `.qmd` (recomendado)

* O arquivo deve renderizar sem erro.
* Preferir caminhos relativos.
* Não depender de objetos no ambiente do RStudio.

### 4.3. Arquivo final (obrigatório)

Entregue **um** arquivo com resultados:

* `respostas.html` **ou**
* `respostas.pdf` **ou**
* `respostas.docx`

---

## 5. Commit com mensagem informativa

Após incluir os arquivos:

```bash
git add exercises/submissions/ex01/<RA>-<sobrenome>
git commit -m "Submissão Ex01 — <RA> <sobrenome>"
```

Exemplo:

```bash
git commit -m "Submissão Ex01 — 123456 Silva"
```

---

## 6. Push e Pull Request

### 6.1. Push da branch

```bash
git push -u origin ex01-<RA>-<sobrenome>
```

### 6.2. Abra o Pull Request (PR)

1. Vá ao seu fork no GitHub.
2. Clique em **Compare & pull request**.
3. Confirme:

   * Base repository: `UFABC-MQ101/mq101-2025`
   * Base branch: `main`
   * Head repository: seu fork
   * Compare branch: `ex01-<RA>-<sobrenome>`
4. Preencha o texto do PR e marque o checklist do template.
5. Clique em **Create pull request**.

---

## 7. Erros comuns

### 7.1. “Funciona no meu computador, mas não no do monitor”

Causas típicas:

* Caminhos absolutos.
* Pacotes faltando.
* Dependência do ambiente do RStudio.

Correção:

* Use caminhos relativos.
* Rode tudo em uma sessão nova do R.
* Inclua `sessionInfo()`.

### 7.2. Arquivos grandes

Evite subir dados brutos enormes e PDFs muito pesados. Prefira:

* Dados mínimos necessários (processados).
* Links para fontes públicas quando aplicável.

---

## 8. Boas práticas de versionamento

* Faça commits pequenos e descritivos.
* Não mexa em arquivos fora da sua pasta.
* Use branches por exercício.
* Não apague o histórico; corrija via commits.

---

## 9. Checklist final (antes do PR)

* [ ] Pasta correta (`exercises/submissions/ex01/<RA>-<sobrenome>/`)
* [ ] `script.R` roda do zero
* [ ] `sessionInfo()` incluído
* [ ] `README.md` explica reprodução
* [ ] Arquivo final (HTML/PDF/DOCX) incluído
* [ ] Nada fora da sua pasta foi modificado
* [ ] Sem dados pessoais sensíveis

---

## 10. Sugestões de aperfeiçoamento (para o curso)

1. Template inicial por exercício (`README.md` + `script.R` + `respostas.Rmd`).
2. Checagens automáticas no PR (estrutura mínima + lint + render opcional).
3. Página “Submissões” no site do curso (GitHub Pages/Quarto).
4. Para turmas grandes, considerar GitHub Classroom para submissões privadas.

```

---

# 2) Como subir o arquivo `exercises/SUBMISSION_GUIDE.md` no GitHub (point and click)

Você fará isso diretamente no site do repositório.

## Passo a passo

1) Acesse:
- https://github.com/UFABC-MQ101/mq101-2025

2) Entre na pasta `exercises/`
- Na lista de arquivos do repositório, clique na pasta **`exercises`**.

3) Crie um arquivo novo
- Clique no botão **Add file** (parte superior direita).
- Selecione **Create new file**.

4) Nomeie o arquivo no caminho correto
No campo de nome do arquivo, digite exatamente:
```

SUBMISSION_GUIDE.md

```
Confirme que você está dentro da pasta `exercises/` (o GitHub mostrará o caminho como `exercises / SUBMISSION_GUIDE.md`).

5) Cole o conteúdo
- Cole o texto completo da seção **(1)** no editor.

6) Faça o commit
Role até o final e preencha:
- **Commit message**: `Adiciona guia de submissão de exercícios`
- Selecione: **Commit directly to the main branch**
- Clique em **Commit new file**

7) Verifique
Volte para a pasta `exercises/` e confirme que o arquivo apareceu:
- `exercises/SUBMISSION_GUIDE.md`

---

## Observação sobre governança
Se a branch `main` estiver protegida para exigir Pull Request, o GitHub pode não permitir “commit direto”. Nesse caso:
- Selecione **Create a new branch for this commit and start a pull request**
- Dê um nome como `add-submission-guide`
- Clique em **Propose new file**
- Abra o PR e faça o merge após aprovação.

---
