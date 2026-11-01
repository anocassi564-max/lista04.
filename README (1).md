 Lista 04 - 2

 1. Revisão da parte 1

1. O contêiner é o elemento pai e os itens são os elementos dentro dele. O `display: flex` é colocado no contêiner.

2. O eixo principal é horizontal, da esquerda para a direita.

 2. Crescer: flex-grow

3. É o espaço que sobra no contêiner. Se todos tiverem `flex-grow: 0`, ninguém ocupa esse espaço.

4. O valor padrão é 0, ou seja, o item não cresce.

5. Mesa: contêiner. Prato: item. Sobra: espaço livre. Peso: valor do `flex-grow`.

6. Usar `flex-grow: 1` no elemento da marca.

7.
- Soma: 2 + 3 + 1 = 6.
- Cada parte: 600 ÷ 6 = 100px.
- Primeiro: 200px.
- Segundo: 300px.
- Terceiro: 100px.

8.
- Espaço ocupado: 300px.
- Sobra: 300px.
- Primeiro: 100px.
- Segundo: 200px.
- Terceiro: 300px.

 3. Encolher: flex-shrink

9. Entra em ação quando falta espaço. O valor padrão é 1.

10.
- Espaço ocupado: 800px.
- Falta: 200px.
- Primeiro item: 300px.
- Segundo item: 300px.

11.
- Primeiro item: 400px.
- Segundo item: 200px.
- Sim, cabe nos 600px.

12. Um menu lateral pode usar `flex-shrink: 0` para não diminuir de tamanho.

4. Tamanho de partida e atalho flex

13. `flex-basis` define o tamanho inicial do item. Nesse caso, vale 10rem (160px, considerando 1rem = 16px).

14. Porque os itens começam com tamanho zero e dividem todo o espaço disponível.

15.
- `flex: initial` = grow 0, shrink 1, basis auto.
- `flex: 1` = grow 1, shrink 1, basis 0%.
- `flex: auto` = grow 1, shrink 1, basis auto.
- `flex: none` = grow 0, shrink 0, basis auto.

16.

Com `flex: 1`:
- Primeiro: 300px.
- Segundo: 300px.

Com `flex: auto`:
- Primeiro: 200px.
- Segundo: 400px.

Os resultados diferem porque `flex: 1` começa com base zero, enquanto `flex: auto` considera o tamanho do conteúdo.

17. Verdadeiro, pois, com conteúdos iguais e mesmas condições, os itens recebem a mesma quantidade de espaço.

 5. O mínimo que trava o encolhimento

18. A propriedade é `min-width: auto`. Para resolver, usamos `min-width: 0`.

19. Quando um texto possui palavras muito longas e ultrapassa o espaço disponível ao lado do menu.

6. order e align-self

20.

a) C, A, B.

b) A, B, C.

c) Porque a ordem visual pode ser diferente da ordem de navegação, causando confusão para quem usa leitores de tela.

21. O valor padrão é 0. O elemento com `order: -1` aparece primeiro.

22.
- `align-self: flex-end`: alinha o item ao final.
- `align-self: auto`: utiliza o alinhamento definido pelo pai.

23. `align-items` alinha todos os itens, enquanto `align-self` alinha apenas um item.

 7. A página com miolo

24.
- `.pagina`: header, miolo e footer.
- `.miolo`: aside e main.

25. Porque `.miolo` precisa organizar seus próprios elementos, o menu e o conteúdo, lado a lado.

26.
- `display: flex`: ativa o Flexbox.
- `flex-direction: column`: organiza os elementos em coluna.
- `min-height: 100vh`: ocupa pelo menos a altura da tela.
- `.miolo { display: flex; }`: organiza o menu e o conteúdo.
- `flex: 1`: ocupa o espaço restante.
- `aside { flex: 0 0 10rem; }`: mantém a largura do menu fixa.
- `main { flex: 1; }`: ocupa o espaço restante.
- `min-width: 0`: permite que o conteúdo diminua.

 8. Erros comuns e síntese

27. O erro é colocar `flex-grow` no contêiner. O correto é aplicar nos elementos filhos.

28.
1. Usar `min-width: 0` para permitir que o item diminua.
2. Usar `flex-wrap: wrap` para passar os itens para outra linha.

29.
- `flex-basis`: define o tamanho inicial.
- `flex-grow`: controla o crescimento.
- `flex-shrink`: controla o encolhimento.
- `order`: define a ordem visual.
- `align-self`: define o alinhamento individual.
