Aluno : Gabriel Fernando de Amorim
Matrícula : 21105496
Disciplina : INE - 02235

Realizei o trabalho sozinho, decidi realiza-lo em gráfico, pois queria aprender a realizar gráficos no Python. 
meu trabalho, diferentemente do enunciado do trabalho final não apresenta os valores de tendencia de alta e queda apenas no cruzamento entre as medias moveis, 
ele apresenta a tendencia em todos os pontos do intervalo definidos pelo usuário, estes podendo ser constantes, alta ou queda. 

O programa que desenvolvi é de fácil utilização, primeiramente o usuário deve inserir a quantidade de valores que deseja adicionar, 
depois ele adiciona os valores na quantidade informada anteriormente, após isso o usuário não precisa mais interferir no programa.

A biblioteca matplotlib foi importada para plotar os gráficos, e as médias moveis que utilizei no trabalho foram as de 3 e 5 sendo elas a curta e a longa respectivamente. 

O trabalho começa com um loop para encontrar a lista com os valores que serão utilizados no trabalho e a print dos valores. 

Após isso definimos variáveis tamanho1 e tamanho2 que nada mais são do que um len(valores), utilizei apenas para testes e deixei as no código porque não interferem e é mais fácil de digitar do que len(valores). 

Depois começa o cálculo das duas medias moveis que explicarei apenas o de uma pois ambas são idênticas apenas alterando a variável janela que nada mais e a quantidade de números que utilizaremos da lista de valores para calcular a média móvel em um valor, durante o cálculo da média móvel calculei primeiramente o primeiro valor obtido no cálculo da média móvel, depois fiz um loop que faz o cálculo para todos os outros valores e obviamente subtrai um valor pois não era necessário calcular novamente o primeiro valor. 
Considerando: somatoria_movel += (valores[i + janela] - valores[i]) 
No código (valores[i + janela] atribui o próximo valor da lista no cálculo da média móvel 
No código - valores[i] move o ultimo ponteiro uma posição para frente 

Durante o cálculo da média móvel de 3 atribui dois números como -1 e na de 5 quatro números como -1, esta atribuição tem como intuito de configura-los como nulo, não pude anula-los durante este período pois durante o cálculo de tendencias estes valores deveriam ser diferentes de nulo, atribui -1 pois é um valor não usual para o cálculo de cotações. 

Depois utilizo a variável valorx, que nada mais e a quantidade de numeros que serão utilizados no intervalo no eixo x do gráfico, não defini datas especificas apenas 
a diferença de cada valor como 1, mas caso necessário podemos variar estes valores para meses, datas, anos etc. (o valorx no início foi definido como -1, mas apenas interfere no primeiro valor que aparece no eixo x do gráfico). 

Após isso começa a parte da definição das tendencia de alta queda e constância, os valores que são iguais a –1, são automaticamente descartados do cálculo da tendencia 
pois possuem pelo menos um valor como nulo, deste modo impossibilitando o cálculo. Caso a média móvel de 3 seja maior que a média móvel de 5 o valor está em alta, caso a média móvel de 3 seja menor que a média móvel de 5 o valor está em queda, 
e caso ambas tenham o mesmo valor ele e constante. 

Depois atribuo os dados da função media_movel1(valores, janela1) que é a média móvel obtida em 3 para mm3 
e a função media_movel2(valores, janela2) para mm5 o intuito destas transformações e transformar os -1 anteriormente fornecidos em valores nulos pois já foi realizado o cálculo das tendencias e não e mais necessário mantê-los em -1, por isso utilizo as funções remove e insert em mm3 e mm5. 

Após isso vem a plotagem do gráfico com a biblioteca matplotlib finalizando o trabalho. 




