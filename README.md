# lista04.

1. O contêiner é o pai. Os itens são os filhos. O display: flex vai no pai.

2. O eixo principal é horizontal, da esquerda para a direita.

2. Crescer: flex-grow

3. Sobra é o espaço vazio que fica no contêiner. Se todos tiverem flex-grow: 0, ninguém ocupa esse espaço.

4. O padrão é flex-grow: 0, ou seja, o item não cresce.

5.

Mesa: contêiner.
Pratos: itens.
Pizza: espaço que sobra.
Peso: valor do flex-grow.

6. Colocar flex-grow: 1 na marca para ela ocupar o espaço que sobra.

7.

Soma: 2 + 3 + 1 = 6.
Cada parte vale 100px.
Resultado: 200px, 300px e 100px.

8.

Sobra: 300px.
Soma: 0 + 1 + 2 = 3.
Cada parte vale 100px.
Resultado: 100px, 200px e 300px.
3. Encolher: flex-shrink

9. O flex-shrink funciona quando falta espaço. O padrão é 1.

10.

Faltam 200px.
Cada item perde 100px.
Resultado: 300px cada.

11.

O primeiro fica com 400px.
O segundo fica com 200px.
Sim, os dois cabem na faixa.

12. Exemplo: logo ou foto de perfil. Usamos flex-shrink: 0 para não deixar diminuir.

4. Tamanho inicial: flex-basis

13. O flex-basis define o tamanho inicial. Ele tem prioridade sobre o width.

14. Com flex-basis: 0, o item começa com tamanho zero e divide o espaço usando o flex-grow.

15.

Atalho	grow	shrink	basis
flex: initial	0	1	auto
flex: 1	1	1	0
flex: auto	1	1	auto
flex: none	0	0	auto

16.

flex: 1: os dois ficam com 300px.
flex: auto: ficam com 200px e 400px.
A diferença é o tamanho inicial de cada item.

17. Falso. flex: 1 deixa os itens iguais. flex: auto considera o tamanho do conteúdo.

5. O mínimo que impede de encolher

18. O min-width: auto impede o item de ficar menor que seu conteúdo. Para permitir diminuir, usamos min-width: 0.

19. Acontece quando existe uma palavra ou link muito grande e o texto acaba saindo da tela.

6. order e align-self

20.

(a) Ordem na tela: C, A, B.
(b) Ordem ao apertar Tab: A, B, C.
(c) Isso importa para acessibilidade e navegação pelo teclado.

21. O padrão é order: 0. O order: -1 aparece primeiro.

22.

align-self: flex-end: vai para baixo e não estica.
align-self: auto: segue o alinhamento do pai.

23.

align-items: alinha todos os itens.
align-self: alinha apenas um item.
7. Página com miolo

24.

.pagina: header, miolo e footer.
.miolo: aside e main.

25. Porque o .miolo também precisa de display: flex para colocar o aside e o main lado a lado.

26.

display: flex: ativa o Flexbox.
flex-direction: column: coloca um item embaixo do outro.
min-height: 100vh: ocupa pelo menos a altura da tela.
flex: 1: ocupa o espaço que sobra.
aside { flex: 0 0 10rem; }: deixa o menu com tamanho fixo.
main { flex: 1; }: ocupa o restante do espaço.
min-width: 0: evita que o texto estoure a página.
8. Erros comuns e resumo

27. Erro: colocar flex-grow no pai. O correto é colocar nos filhos.

28.

min-width: 0: evita que o texto estoure.
flex-wrap: wrap: permite que os itens passem para a linha de baixo.

29.

flex-basis: tamanho inicial.
flex-grow: crescer.
flex-shrink: encolher.
order: mudar a ordem visual.
align-self: alinhar apenas um item.
Para decorar mais facilmente
flex-grow = crescer.
flex-shrink = diminuir.
flex-basis = tamanho inicial.
order = ordem.
align-items = alinha todos.
align-self = alinha um sozinho.
min-width: 0 = permite encolher.
flex-wrap = quebra para outra linha.
