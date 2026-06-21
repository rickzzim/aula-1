# aula-1
Este notebook Colab explora conceitos fundamentais no processamento de sinais de áudio, abrangendo desde a geração de tons puros e sinais chirp até a simulação acústica de ambientes utilizando convolução. Ele serve como uma ferramenta prática para visualizar e ouvir como diferentes parâmetros de áudio afetam a percepção sonora e as representações no domínio do tempo.

Conteúdo do Notebook:
1. Geração e Análise de Sinais de Tom Puro (Ondas Senoidais)
Objetivo: Gerar e visualizar ondas senoidais com frequências específicas (500 Hz, 5000 Hz, 10000 Hz).
Experimento: Observa-se como o aumento da frequência resulta em mais oscilações no mesmo intervalo de tempo, tornando o som percebido mais agudo.
Ferramentas: numpy para geração de sinais, matplotlib.pyplot para visualização e scipy.io.wavfile junto com IPython.display.Audio para reprodução e salvamento em formato WAV.
2. Geração e Análise de Sinais Chirp
Objetivo: Criar e analisar sinais chirp, onde a frequência varia gradualmente ao longo do tempo.
Experimento: São gerados três tipos de chirp: linear, quadrático e logarítmico (exponencial), cada um com uma variação de frequência de 500 Hz a 10000 Hz. A visualização e a audição desses sinais demonstram como a frequência inicial grave se transforma em uma frequência final aguda, com diferentes curvas de aceleração de frequência.
Ferramentas: scipy.signal.chirp é a função principal para a geração desses sinais.
3. Análise e Reprodução de Arquivos de Áudio (Domínio do Tempo)
Objetivo: Carregar e visualizar o domínio do tempo de arquivos WAV existentes (handel.wav, h_banheiro.wav, sinal_taca.wav).
Experimento: Demonstra-se como a alteração da frequência de reprodução (rate no IPython.display.Audio) impacta a percepção do áudio: frequências maiores aceleram e tornam o som mais agudo; frequências menores o desaceleram e tornam mais grave. Isso ilustra o conceito de taxa de amostragem na reprodução.
Ferramentas: scipy.io.wavfile.read para leitura de arquivos WAV.
4. Simulação Acústica Via Convolução
Objetivo: Simular o efeito acústico de um ambiente (representado por uma resposta ao impulso, h_banheiro.wav) em um sinal de áudio (sinal_taca.wav).
Experimento: A convolução de um sinal de áudio com a resposta ao impulso de um banheiro (h_banheiro.wav) é realizada. O resultado é um sinal que simula como o som da taça seria percebido dentro de um ambiente com as características acústicas do banheiro (reverberação e eco). O gráfico resultante mostra um prolongamento e múltiplas reflexões no sinal.
Conceito: A convolução é uma operação fundamental em processamento de sinais para modelar a interação de um sinal com um sistema linear e invariante no tempo (LTI), como um ambiente acústico.
Ferramentas: scipy.signal.convolve para realizar a convolução.
Como Usar:
Execute as Células: Basta executar as células sequencialmente para observar a geração dos sinais, os gráficos no domínio do tempo e ouvir os exemplos de áudio.
Experimente: Altere os parâmetros dos sinais (frequência, duração, taxas de amostragem) e as taxas de reprodução para entender melhor seus efeitos.
Explore: Os arquivos .wav utilizados (handel.wav, h_banheiro.wav, sinal_taca.wav) são carregados do ambiente do Colab e representam diferentes tipos de áudio e respostas ao impulso.
