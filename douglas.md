# Respostas aos Exercícios - Capítulo 1

## Exercício 1.2 - O que acontece sem…?

1. **Sem `<!DOCTYPE html>`:**
   * Na consola (`document.compatMode`), o valor que aparece é `BackCompat` (Quirks mode).
   * No ficheiro original (com a tag), o valor é `CSS1Compat` (Standards mode).

2. **Sem `<meta charset="utf-8">`:**
   * Ao guardar o ficheiro com a codificação *Windows-1252*, os acentos e caracteres especiais ficam desconfigurados. O browser não sabe como interpretar a codificação correta sem esta tag.

3. **Sem `<meta name="viewport">`:**
   * Em modo de dispositivo móvel, o texto fica minúsculo. O telemóvel simula um ecrã de desktop (geralmente 980px) em vez de adaptar a página à largura real do ecrã do dispositivo.

## Exercício 1.3 - O parser corrige por si

* **Onde apareceram `<html>`, `<head>` e `<body>`?**
  Apareceram na árvore DOM (separador *Elements* das ferramentas de programador). O browser inseriu-as automaticamente para corrigir a ausência destas tags no código-fonte original.
* **O que fez o browser com as tags `<b>` e `<i>` mal aninhadas?**
  O motor do browser reorganizou e fechou as tags automaticamente para tentar manter uma hierarquia válida no HTML.
* **Para onde foi o parágrafo que estava dentro da tabela?**
  O browser ejetou o parágrafo `<p>` para fora da tabela, colocando-o imediatamente antes da `<table>`. Um parágrafo não é permitido diretamente dentro de uma tabela a menos que esteja dentro de uma célula de dados (`<td>`).
* **Porque é que isto prova que o browser não mostrar erros não significa que o HTML esteja correto?**
  Porque o browser tenta "adivinhar" e corrigir a estrutura em tempo real para apresentar a página ao utilizador, mascarando os nossos erros de sintaxe. É por isso que é obrigatório usar validadores externos para garantir que o código está realmente correto.