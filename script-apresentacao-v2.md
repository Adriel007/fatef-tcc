# Script rápido da apresentação (slides v2)

Cerca de 5 minutos, falando de forma natural. Cada bloco é o que dizer no slide.

**1. Capa**
Bom dia. Vou mostrar o que descobri ao abrir uma inteligência artificial por dentro, para ver se uma IA encolhida, chamada ternária, resolve uma tarefa do mesmo jeito que a versão completa.

**2. Como uma IA de texto funciona**
Uma IA de texto adivinha a próxima palavra. Ela acerta porque tem bilhões de números ajustados no treino, e cada um, em geral, ocupa 16 bits de memória.

**3. Encolher a IA**
Para gastar menos memória, dá para guardar cada número com menos bits, como um arredondamento. Isso se chama quantização. No caso estudado, vai de 16 bits para 1,58 bit, cerca de 10 vezes menos.

**4. O caso ternário**
No modelo ternário, cada peso só pode ser menos um, zero ou mais um. O modelo se chama BitNet, e os autores dizem que a qualidade é comparável à da versão completa. Essa é a afirmação deles, não uma medida minha.

**5. A pergunta do trabalho**
A pergunta é: por dentro, a IA ainda resolve o problema do mesmo jeito? A hipótese era que mudam os números, mas o passo a passo continua o mesmo.

**6. Abrindo a caixa-preta**
Normalmente vemos só a entrada e a saída. A interpretabilidade mecânica abre a caixa e procura as partes que fazem cada tarefa: blocos grandes, os componentes, e peças pequenas, as cabeças. Um conjunto delas forma um circuito.

**7. A tarefa de teste**
Usei uma tarefa simples: em "Maria e João foram à loja. João deu o livro para...", a resposta é Maria. A IA precisa copiar o nome certo e suprimir o repetido. Esse circuito já foi descrito em um modelo completo, então há com o que comparar.

**8. Como comparamos**
Para comparar bem eu precisaria de um gêmeo de precisão total, e o BitNet não tem. Usei dois pares substitutos, parecidos mas não iguais: o Spectra e um modelo pequeno que treinei nas duas versões.

**9. O que achamos no BitNet**
Encontrei três cabeças: duas copiam o nome certo e uma suprime o repetido. Em 83 pares de frases, ficaram de 98 a 360 vezes acima do ruído. É compatível com o circuito conhecido, mas, sem gêmeo, não há número de comparação.

**10. Só no Spectra**
Estes números são do Spectra, não do BitNet, e de uma única execução. A importância dos blocos segue a mesma tendência, 0,93. A ordem coincide menos, 0,51, e os 30 mais importantes coincidem em parte, 0,43. É um indício, não uma prova.

**11. No modelo pequeno**
No modelo pequeno, nenhum traço interno é exclusivo de uma versão: são zero. O alinhamento de direção é baixo, 0,12, e o piso é 0,00. Isso sugere que os traços estão guardados em outra orientação. A figura é só uma analogia, e vale só para esse modelo.

**12. O que ainda não sabemos**
A comparação por cabeça ficou inconclusiva, porque o teste de confiabilidade falhou: 0,053 e 0,057, contra o limite de 0,05. O Spectra é parecido com o BitNet, não igual, e foi uma única execução.

**13. Os números do trabalho**
Aqui estão os seis números principais, cada um com o modelo de origem. Lembrando que os do Spectra e do modelo pequeno não são do BitNet.

**14. Conclusão**
Os resultados sustentam a hipótese em parte. Nos blocos e nos traços internos, o jeito de resolver parece se manter. Por cabeça, ficou inconclusivo. O próximo passo é repetir a comparação com um teste de confiabilidade aprovado.

**15. Obrigado**
Obrigado. Fico à disposição para as perguntas.

**16 e 17. Reservas (só se perguntarem)**
Tabelas de apoio com todos os números do BitNet e dos outros modelos, tiradas do capítulo de Resultados.
