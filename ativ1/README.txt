Bisseção

1. Inicialização

A função bisectionMethod(f, a, b, toler, iterMax) recebe:

f: a função a ser analisada.

a e b: extremos do intervalo inicial.

toler: tolerância para o critério de parada.

iterMax: número máximo de iterações.

Calcula fa = f(a) e fb = f(b).

Se fa * fb > 0, significa que não há mudança de sinal → não há raiz garantida no intervalo, e a função retorna um erro.

--

2. Laço principal (método da bisseção)

O ponto médio 𝑥 do intervalo é calculado:

x = (a+b) / 2

Calcula fx = f(x).

Exibe no console os valores atuais dos limites, x, fx e deltaX.

--

3. Critérios de Parada

Se deltaX e |fx| forem menores ou iguais à tolerância OU se o número máximo de iterações for atingido, o laço para e raiz recebe x.

--

4. Atualização do intervalo

Se fa * fx > 0, significa que fa e fx têm o mesmo sinal → a raiz não está no intervalo [a,x], então atualiza a = x e fa = fx.

Caso contrário, a raiz está em [x,b], então apenas b = x.

deltaX é atualizado (deltaX /= 2).

Incrementa o contador de iterações.

--

5. Verificação final

Se a precisão foi alcançada, condErro recebe 0 (indica sucesso), caso contrário, mantém 1 (indica erro ou parada por iteração máxima)