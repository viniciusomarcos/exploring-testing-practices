# Explorando Práticas de Teste

Neste exercício, vamos explorar práticas de teste em sistemas reais utilizando a ferramenta [TestMiner](https://andrehora.github.io/testminer).

O TestMiner permite visualizar e analisar testes de software em repositórios do GitHub, fornecendo dados sobre como os projetos organizam seus testes, como eles evoluem entre versões e quais bibliotecas de teste são utilizadas.
Explore a ferramenta antes de começar para se familiarizar com seu funcionamento.

Mais detalhes no GitHub da ferramenta: https://github.com/andrehora/testminer.

---

## Passo 1: Selecionar um repositório

Escolha um repositório real que possua testes de software.
Abaixo estão alguns links para ajudá-lo a encontrar projetos interessantes:

- Python: https://github.com/topics/python?l=python
- JavaScript: https://github.com/topics/javascript?l=javascript
- TypeScript: https://github.com/topics/typescript?l=typescript
- Java: https://github.com/topics/java?l=java

- Tópicos: [ai](https://andrehora.github.io/testminer/#topic:ai), [llm](https://andrehora.github.io/testminer/#topic:llm), [api](https://andrehora.github.io/testminer/#topic:api), [nodejs](https://andrehora.github.io/testminer/#topic:nodejs), [android](https://andrehora.github.io/testminer/#topic:android)

- Por organização: [Google](https://andrehora.github.io/testminer/#google), [Microsoft](https://andrehora.github.io/testminer/#microsoft), [Apple](https://andrehora.github.io/testminer/#apple), [Facebook](https://andrehora.github.io/testminer/#facebook), [Netflix](https://andrehora.github.io/testminer/#netflix), 
[GitHub](https://andrehora.github.io/testminer/#github), [Apache](https://andrehora.github.io/testminer/#apache), [HuggingFace](https://andrehora.github.io/testminer/#huggingface)

## Passo 2: Explorar o repositório selecionado

Busque o repositório escolhido no [TestMiner](https://andrehora.github.io/testminer) e analise os dados de teste gerados pela ferramenta.

## Passo 3: Explicar uma prática de teste

Escolha uma prática ou dado de teste relevante e explique com suas próprias palavras.

---

## Instruções de entrega

1. Faça um `fork` deste repositório (saiba mais sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork. Pode adicionar imagens para enriquecer sua explicação.
3. No Moodle, submeta apenas a URL do seu fork.

---

### Respostas

Repositório: https://github.com/browser-use/browser-use  
URL TestMiner: https://andrehora.github.io/testminer/#browser-use  

**Explicação:**

Ao analisar o projeto no TestMiner, foquei em dois pontos principais: a organização dos arquivos de teste e a evolução deles ao longo das versões.

Na seção de **Test Location**, fica evidente que o repositório adota a prática de manter os testes isolados da aplicação principal. Dos 84 testes identificados, 83 estão concentrados na pasta raiz `tests`, e apenas arquivos pontuais ficam em outros diretórios. Olhando as categorias destacadas no painel (`llm`, `cli`, `action`, `click`), nota-se que os testes foram estruturados para cobrir individualmente as ações do agente e as interações no navegador, permitindo validar comandos isolados sem precisar executar o sistema inteiro.

Além disso, o gráfico de **Test History** mostra a evolução da suíte ao longo do ciclo de vida do projeto: na versão inicial (`0.1.0`), havia menos de 10 testes cadastrados; na versão intermediária (`0.5.6`), esse número subiu para cerca de 60; e na versão recente (`0.13.11`), já ultrapassa a marca de 130 testes. Esse crescimento contínuo demonstra que a escrita de testes acompanhou a maturidade da ferramenta, garantindo estabilidade e evitando regressões à medida que novas integrações com navegadores e LLMs foram adicionadas.

![Localização dos testes no TestMiner](https://raw.githubusercontent.com/viniciusomarcos/exploring-testing-practices/main/img/test_location.png)

![Crescimento dos testes ao longo das releases](https://raw.githubusercontent.com/viniciusomarcos/exploring-testing-practices/main/img/teste_history.png)
