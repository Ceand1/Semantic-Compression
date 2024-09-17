# `Compressão Semântica`
# `Semantic Compression`

## Apresentação

O presente projeto foi originado no contexto das atividades da disciplina de pós-graduação *IA376N - IA generativa: de modelos a aplicações multimodais*, 
oferecida no segundo semestre de 2024, na Unicamp, sob supervisão da Profa. Dra. Paula Dornhofer Paro Costa, do Departamento de Engenharia de Computação e Automação (DCA) da Faculdade de Engenharia Elétrica e de Computação (FEEC).


> |Nome  | RA | Especialização|
> |--|--|--|
> | Antonio César de Andrade Júnior  | 245628  | Eng. de Computação |
> | Eduardo Nunes Velloso  | 290885  | Eng. Elétrica |


## Descrição Resumida do Projeto

A compressão de dados, e em particular a compressão de imagens, é um componente fundamental para as novas gerações de comunicação móvel.
Aplicações de natureza crítica, como a telemedicina e os carros autônomos, envolvem decisões que precisam ser tomadas imediatamente com base em uma transmissão de imagens contínua, proveniente de vários sensores simultâneamente.
Para viabilizar essas aplicações, uma compressão a taxas extremamente baixas (menos de 0.1 bit por pixel ou bpp) se faz necessária.
Embora nesse caso já não seja possível preservar o conteúdo estrutural das imagens, essas tarefas estão interessadas somente em certos atributos da imagem, os quais constituem o valor semântico embutido na imagem.

A tarefa da compressão semântica, portanto, é a de projetar um codificador capaz de extrair essa informação semântica e um decodificador capaz de gerar uma imagem reconstruída com o mesmo conteúdo essencial.
O projeto de tais decodificadores pode ser desenvolvido por meio de modelos generativos.

Em [[1]](#1), os autores introduziram uma proposta inicial da utilização de GANs para compressão semântica, tanto utilizando segmentação semântica para sintetizar regiões de interesse (por exemplo, para sintetizar fundos de videochamadas) quanto comprimindo apenas uma sequência de bits (por exemplo, para sintetizar detalhes de partes da imagem).
O trabalho de [[2]](#2) propôs uma arquitetura chamada DSSLIC, também utilizando GANs, que combina a utilização dos mapas semânticos com os resíduos da própria compressão como entradas da rede decodificadora.
Já em [[3]](#3), é utilizado um modelo de difusão latente (LDM), codificando um colormap quantizado da imagem original para auxiliar na reconstrução a partir do vetor semântico extraído.

Este projeto tem como objetivo realizar um estudo comparativo de modelos de compressão semântica baseados nos mencionados acima.

[Link para o vídeo de apresentação](https://drive.google.com/file/d/1sVEZiwOKVfSp3zXrToVWvKQgVfOdiWUl/view?usp=sharing)

[Link para a apresentação de slides](https://drive.google.com/file/d/1XXuT1HYH33gW0SCd8A1U8ulIU7ICBDPW/view?usp=sharing)

## Metodologia Proposta
> Para a primeira entrega, a metodologia proposta deve esclarecer:
> * Qual(is) base(s) de dado(s) o projeto pretende utilizar, justificando a(s) escolha(s) realizadas.
> * Quais abordagens de modelagem generativa o grupo já enxerga como interessantes de serem estudadas.
> * Artigos de referência já identificados e que serão estudados ou usados como parte do planejamento do projeto
> * Ferramentas a serem utilizadas (com base na visão atual do grupo sobre o projeto).
> * Resultados esperados
> * Proposta de avaliação dos resultados de síntese

## Cronograma
>| Tarefa          | Data de Finalização     | Número de Semanas| Progresso  |
>|-----------------|------------|-----------|------------|
>| Revisão bibliográfica        | 17/09/2024 | 2 | ██████████ 100% |
>| Desenvolvimento do encoder (1º versão)| 24/09/2024 | 1 | ░░░░░░░░░░ 0% |
>| Método 1    | 08/10/2024 | 2 | ░░░░░░░░░░ 0%  |
>| Entrega 2          | 08/10/2024 | 0 | ░░░░░░░░░░ 0% |
>| Desenvolvimento do encoder (Versão Final)| 15/10/2024 | 1 | ░░░░░░░░░░ 0% |
>| Método 2    | 29/10/2024 | 2 | ░░░░░░░░░░ 0%  |
>| Método 3    | 12/11/2024 | 2 | ░░░░░░░░░░ 0%  |
>| Análise dos resultados    | 25/11/2024 | 2 | ░░░░░░░░░░ 0%  |
>| Montar entrega 3   | 25/11/2024 | 0 | ░░░░░░░░░░ 0%  |

## Referências Bibliográficas
> Apontar nesta seção as referências bibliográficas adotadas no projeto.

<a id="1">[1]</a> : T. Bachard and T. Maugey, "Can Image Compression Rely on CLIP?," in IEEE Access, vol. 12, pp. 78922-78938, 2024, doi: 10.1109/ACCESS.2024.3408651., https://ieeexplore.ieee.org/abstract/document/10545425

<a id="2">[2]</a> : T. Bachard, T. Bordin and T. Maugey, "CoCliCo: Extremely Low Bitrate Image Compression Based on CLIP Semantic and Tiny Color Map," 2024 Picture Coding Symposium (PCS), Taichung, Taiwan, 2024, pp. 1-5, doi: 10.1109/PCS60826.2024.10566358., https://ieeexplore.ieee.org/document/10566358

<a id="3">[3]</a> : T. Bordin and T. Maugey, "Semantic Based Generative Compression of Images for Extremely Low Bitrates," 2023 IEEE 25th International Workshop on Multimedia Signal Processing (MMSP), Poitiers, France, 2023, pp. 1-6, doi: 10.1109/MMSP59012.2023.10337734., https://ieeexplore.ieee.org/document/10337734