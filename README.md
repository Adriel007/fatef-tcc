# fatef-tcc · demo visual (modo apresentação)

Demo 3D de apoio ao TCC de Sistemas de Informação (FATEF São Vicente):
**"Interpretabilidade mecanicista em modelos de linguagem ternários: um circuito IOI no BitNet b1.58"**.

## O que é

Uma animação em Three.js, com câmera automática, que mostra por dentro o caminho de uma pergunta até a resposta de um modelo de linguagem: codificação do texto (tokens), embeddings, pesos, as camadas empilhadas e a escolha de cada palavra da resposta. Dá para pausar, voltar e avançar passos.

O objetivo é **mostrar as diferenças de arquitetura entre um modelo de precisão total (FloatLM 2,4B) e um modelo ternário, com pesos em {−1, 0, +1} (TriLM 2,4B)**, ambos da família Spectra. O foco é o processo, não a qualidade da resposta.

- `index.html`: a animação, com o botão para alternar entre Precisão total e Ternário.
- `compare.html`: comparativo lado a lado das duas arquiteturas.

Os resultados do circuito IOI no BitNet b1.58 estão no TCC. Esta demo **não** reproduz essa análise.

## Por que não é um chat ao vivo

Tudo aqui são **gravações de execuções reais** dos dois modelos, reproduzidas no navegador. Nada é digitado nem calculado na hora. As razões:

1. **Hardware da apresentação.** O computador da faculdade é Windows 10, 16 GB de RAM, sem GPU. Os dois modelos juntos pedem cerca de 10 GB só de pesos, e em CPU cada resposta demora dezenas de segundos. Esse número vem do LEIA-ME do projeto e **não foi testado nesse computador**.
2. **Previsibilidade.** Uma demonstração diante da banca não pode depender de carregar modelos, de memória livre ou de a resposta sair diferente do ensaio. A gravação sempre se comporta igual.
3. **Funciona offline.** São só arquivos estáticos (cerca de 2,7 MB): abrem por duplo clique ou em qualquer hospedagem, sem Python, sem instalar nada e sem baixar os modelos.

As gravações foram feitas com os modelos reais em GPU, e os números e palavras que aparecem na tela vêm dessas execuções.

## Como as perguntas foram escolhidas (limitação)

São 6 perguntas em português. Os modelos são **base** (não foram ajustados para conversar) e treinados em texto majoritariamente em inglês. Das 32 perguntas testadas em português, só cerca de 11 tiveram resposta correta nos dois modelos, e a demo usa as perguntas dessa lista. A escolha foi feita pelo resultado, para a banca não ver um modelo errar por motivo alheio ao assunto. **Isto não é uma medida da qualidade dos modelos**: a demo não serve para comparar quem acerta mais.

## Status

Testado em Chrome (headless, Linux). **Não foi testado em Windows/Edge.**
