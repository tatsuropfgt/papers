# MIR
## Symbolic Music Generation
Infilling Piano Performances [[NeurIPS workshop18, [#40](https://github.com/InabaTatsuro/papers/issues/40)]
- infill deleted section of MIDI by using the transformer
- give {left context + special token + right context} to the model and generate the blanks

FIGARO: Generating Symbolic Music with Fine-Grained Artistic Control [ICLR23, [#39](https://github.com/InabaTatsuro/papers/issues/39)]
- FIne-grained music Generation via Attention-based, RObust control (FIGARO) by applying description-to-sequence modelling
- combine learned high-level features with domain knowledge which acts as a strong inductive bias

Exploring the Efficacy of Pre-trained Checkpoints in Text-to-Music Generation Task [AAAI23 workshop, [#38](https://github.com/InabaTatsuro/papers/issues/38)]
- given text, generate symbolic music using pre-trained language models like BERT, GPT-2, and BART
- the model that initializes the parameters by BART outperformed the model that initializes parameters randomly

Mubert [[github](https://github.com/MubertAI/Mubert-Text-to-Music)]
- generate music from free text prompt
- this is not actual generation, but just combine the pre-composed music according to the rule

Vector Quantized Contrastive Predictive Coding for Template-based Music Generation [20, [#36](https://github.com/InabaTatsuro/papers/issues/36)]
- given a template sequence, generate novel sequences sharing perceptible similarities with the original template
- encode and quantize the template sequence followed by decoding to generate variations

MMM : Exploring Conditional Multi-Track Music Generation [ArXiv20, [#34](https://github.com/InabaTatsuro/papers/issues/34)]
- Multitrack inpainting, using event level token representation and transformer
- replace the sequences of the bar representation which we want to predict into the token, and add the token to the last
- no quantitative results, only method and demo

Multitrack Music Transformer [ICASSP23][[#29](https://github.com/InabaTatsuro/papers/issues/29)]
- propose MMT, multitrack music representation for symbolic music generation can reduce memory usage
- multitrack symbolic music generation by using MMT
  - Continuation, scratch generation, instrument informed generation

Compound word transformer: Learning to compose full-song music over dynamic directed hypergraphs [AAAI21][[#27](https://github.com/InabaTatsuro/papers/issues/27)]
- group consecutive and related tokens into compound words to capture the co-occurrence relationship
- 5-10 times faster at training with comparable quality
- CP transformer can be seen as the hyperedge prediction

PopMAG: Pop Music Accompaniment Generation [[ACM20](https://arxiv.org/abs/2008.07703)][[#26](https://github.com/InabaTatsuro/papers/issues/26)]
- Multitrack-MIDI representation (MuMIDI) enables simultaneous multi-track generation in a single sequence
- model multiple note attributes of a musical note in one step and use the architecture of transformerXL to capture the long-term dependencies

Controllable deep melody generation via hierarchical music structure representation [[ISMIR21](https://arxiv.org/abs/2109.00663)][[#24](https://github.com/InabaTatsuro/papers/issues/24)]
- music framework generates rhythm and basic melody using two separate transformer-based networks
- then, generate the melody conditioned on the basic melody, rhythm, and chords

A Hierarchical Latent Vector Model for Learning Long-Term Structure in Music [[ICML18](https://arxiv.org/abs/1803.05428)][[#23](https://github.com/InabaTatsuro/papers/issues/23)]
- hierarchical decoder which first outputs embeddings for sub-sequences and then uses these embeddings to generate each subsequence
- propose MusicVAE which uses the hierarchical latent vector model

PopMNet: Generating structured pop music melodies using neural networks [[Wu+, 19](https://www.sciencedirect.com/science/article/abs/pii/S000437022030062X)]
- CNN generate melody structure which is defined by pairwise relations, specifically and the sequence between all bars in a melody
- RNN generate melodies conditioned on the structure and chord progression

A Hierarchical Recurrent Neural Network for Symbolic Melody Generation [[IEEE](https://arxiv.org/abs/1712.05274)]
- factor melody generation into 3 sub-problems and each sub-problem is solved by each LSTM

MELONS: generating melody with long-term structure using transformers and structure graph [[ICASSP22](https://arxiv.org/abs/2110.05020)][[#22](https://github.com/InabaTatsuro/papers/issues/18)]
- factor melody generation into 2 sub-problems: structure generation and structure conditional melody generation
- these sub-problems are solved by the linear transformer

Pop Music Transformer: Beat-based Modeling and Generation of Expressive Pop Piano Compositions [[ACM20](https://arxiv.org/abs/2002.00212)][[#20](https://github.com/InabaTatsuro/papers/issues/20)]
- propose REMI, new event representation of beat-based music
- use Auto Transcription to get enough training data

Museformer [[Yu+ NeurIPS22](https://arxiv.org/abs/2210.10349)][[#11](https://github.com/InabaTatsuro/papers/issues/11)]
- Use fine- and coarse-grained attention for music generation
- fine-grained attention captures the tokens in the most relevant measure (the previous 1,2,4,8...)
- coarse-grained attention captures the summarization of the other measure, which reduces the computational cost

Music Transformer [[Huang+, ICLR19](https://arxiv.org/abs/1809.04281)][[#10](https://github.com/InabaTatsuro/papers/issues/10)]
- Generate symbolic music by transformers with relative position-based attention
- reduce the memory requirements in relative position-based attention by "skewing"

Graph-based Polyphonic Multitrack Music Generation [[Cosenza+, 23/7](https://arxiv.org/abs/2307.14928)][[#1](https://github.com/InabaTatsuro/papers/issues/1)]
- Use graph to represent multitrack music score
- Train GCN and VAE to generate graph (music)
- Not good performance

## Symbolic Music Understanding
PiRhDy: Learning Pitch-, Rhythm-, and Dynamics-aware Embeddings for Symbolic Music[ACM20][[#30](https://github.com/InabaTatsuro/papers/issues/30)]
- generate music note embeddings
- (1) token modeling: separately represents pitch, rhythm, and dynamics and integrates them into a single token embedding
- (2) context modeling: use melodic and harmonic embedding to train the token embedding

MusicBERT: Symbolic Music Understanding with Large-Scale Pre-Training [[ACL finding21](https://aclanthology.org/2021.findings-acl.70/)][[#28](https://github.com/InabaTatsuro/papers/issues/28)]
- Pre-train BERT with 1.5M MIDI files which is private and created by the Microsoft Research Asia
- use OctupleMIDI encoding and bar-level masking strategy to enhance symbolic music data

Graph Neural Network for Music Score Data and Modeling Expressive Piano Performance [[Jeong+, ICML19](https://proceedings.mlr.press/v97/jeong19a.html)][[[#6](https://github.com/InabaTatsuro/papers/issues/6)]]
- Use GNN and LSTM with Hierarchical Attention Network to generate expressive piano performance
- GNN captures the nodes information in a measure and LSTM w/HAN captures the measures information
- Let the node have nodes information in other measures by updating iteratively

### Survey
A Survey on Deep Learning for Symbolic Music Generation [[ACM23/8](https://dl.acm.org/doi/abs/10.1145/3597493)][[#25](https://github.com/InabaTatsuro/papers/issues/25)]

A Survey of AI Music Generation Tools and Models [[Zhu+, 23/8](https://arxiv.org/abs/2308.12982)][[#12](https://github.com/InabaTatsuro/papers/issues/12)]

## Audio Music Generation
ERNIE-Music: Text-to-Waveform Music Generation with Diffusion Models [AACLdemo23, [#37](https://github.com/InabaTatsuro/papers/issues/37)]
- use the diffusion model to generate music conditioned by free-form text
- outperform the previous models in terms of text-music relevance and music quality, as judged by human

## Read Later
Modeling temporal tonal relations in polyphonic music through deep networks with a novel image-based representation [[Chuan+, AAAI18](https://ojs.aaai.org/index.php/AAAI/article/view/11880)]
- mugic generation, convolution

Counterpoint by Convolution [[Huang+, ISMIR17](https://arxiv.org/abs/1903.07227)]
- music generation, convolution, inpainting, Gibbs sampling

Musicaiz: A python library for symbolic music generation, analysis and visualization [[Olivan+, 23](https://carlosholivan.github.io/musicaiz/)]
- Python の Symbolic Music Generation 用ライブラリ

Cadence Detection in Symbolic Classical Music using Graph Neural Networks [[Karystinaios+, ISMIR22](https://arxiv.org/abs/2208.14819)]

VirtuosoTune: Hierarchical Melody Language Model [[Jeong, 23](http://ieiespc.org/AURIC_OPEN_temp/RDOC/ieie03/ieietspc_202308_006.pdf)]

Noise2Music: Text-conditioned Music Generation with Diffusion Models [[[Huang+, 23/2](https://arxiv.org/abs/2302.03917)]]

Transformer vae: A hierarchical model for structure-aware and interpretable music representation learning [[Jiang+, ICASSP20](https://ieeexplore.ieee.org/document/9054554)]

- Music VAE
- NSynth
- MuseNet
- SDMuse

# NLP
## Text Generation
InCoder: A Generative Model for Code Infilling and Synthesis [ICLR23][[#32](https://github.com/InabaTatsuro/papers/issues/32)]
- InCoder can infill the program via left-to-right generation
- train by maximizing logP([left; <mask>; right; <mask>; span; <EOM>]) and inference by sampling tokens autoregressively from the distributions P(・| [left; <mask>; right; <mask>])

Contrastive Decoding: Open-ended Text Generation as Optimization[ACl23, [#41](https://github.com/InabaTatsuro/papers/issues/41)]
- decoding with maximum probability often results in short and repetitive text and sampling can often produce incoherent text
- Contrastive Decoding (CD) is a reliable approach that optimizes a contrastive objective subject to a plausibility constraint


## Text Classification
Hierarchical Attention Networks for Document Classification [[Yang+, 16](https://www.cs.cmu.edu/~./hovy/papers/16HLT-hierarchical-attention-networks.pdf)][[#8](https://github.com/InabaTatsuro/papers/issues/8)]
- HAN can capture the insights of the hierarchical structure (words form sentences, sentences form a document) and the difference in importance of each word and sentence

## Sentence Embedding
WhitenedCSE: Whitening-based Contrastive Learning of Sentence Embeddings [[Gao+, ACL23](https://arxiv.org/abs/2104.08821)][[#5](https://github.com/InabaTatsuro/papers/issues/5)]
- SimCSE + whitening
- whitening means the transformation of the data to have a mean of zero and a covariance matrix of the identity matrix

## Positional embedding
On Positional embeddings in BERT [ICLR21][[#31](https://github.com/InabaTatsuro/papers/issues/31)]
- analyze Positional Embeddings (PEs) based on 3 properties, translational invariance, monotonicity, and symmetry
- breaking translational invariance and monotonicity degrades downstream task performance while breaking symmetry improves downstream task performance
- fully learnable absolute position embedding generally improves performance on the classification task, while relative position embedding improves performance on the span prediction task

## Read Later
Locating and Editing Factual Associations in GPT [[Meng+, NeurIPS22](https://openreview.net/forum?id=-h6WAS6eE4)]

Mass-Editing Memory in a Transformer [[Meng+, ICLR23](https://openreview.net/forum?id=MkbcAHIYgyS)]
- the research after "Locating and Editing Factual Associations in GPT"

# ML
## Attention, graph
Do Transformers Really Perform Bad for Graph Representation? [[NeurIPS21](https://arxiv.org/abs/2106.05234)][[#21](https://github.com/InabaTatsuro/papers/issues/21)]
- propose Graphormer, which is based on the standard Transformer and can utilize the structural information of a graph
- similar to [#18](https://github.com/InabaTatsuro/papers/issues/18)

GaAN: Gated Attention Networks for Learning on Large and Spatiotemporal Graphs [[Zhang+, 18](https://arxiv.org/abs/1803.07294)] [[#19](https://github.com/InabaTatsuro/papers/issues/19)]
- use a convolutional sub-network to control each attention head's weight

Global Self-Attention as a Replacement for Graph Convolution [[KDD22](https://arxiv.org/abs/2108.03348)][[#18](https://github.com/InabaTatsuro/papers/issues/18)]
- add edge information to the self-attention calculation

Graph Transformer Networks [[Yun+, NeurIPS19](https://arxiv.org/abs/1911.06455)][[#17](https://github.com/InabaTatsuro/papers/issues/17)]
- generate new meta-path which represents multi-hop relations and new-graph structure by multiplication of different adjacency matrix
- can be applied to heterogeneous graph

Graph Transformer [[Li+, 18](https://openreview.net/forum?id=HJei-2RcK7)][[#16](https://github.com/InabaTatsuro/papers/issues/16)]
- evolve target graph by recurrently applying source-attention from source graph and self-attention from target graph
- they can have different structure

Attention Guided Graph Convolutional Networks for Relation Extraction [[Guo+, ACL19](https://aclanthology.org/P19-1024/)][[#15](https://github.com/InabaTatsuro/papers/issues/15)]
- transform the original graph to a fully connected edge-weighted graph by self-attention

Multi-hop Attention Graph Neural Networks [[Wang+, IJCAI21](https://www.ijcai.org/proceedings/2021/425)][[#14](https://github.com/InabaTatsuro/papers/issues/14)]
- compute attention weights on edges, then compute self-attention weight between disconnected nodes
- can capture the long-range dependencies

On the Global Self-attention Mechanism for Graph Convolutional Networks[[Wang+, IEEE20](https://arxiv.org/abs/2010.10711)][[#13](https://github.com/InabaTatsuro/papers/issues/13)]
- Apply Global self-attention (GSA) to GCNs
- GSA allows GCNs to capture feature-based vertex relations regardless of edge connections

Self-Attention with Relative Position Representations [[Shaw, NAACL18](https://arxiv.org/abs/1803.02155)][[#9](https://github.com/InabaTatsuro/papers/issues/9)]
- extend self-attention to consider the pairwise relationships between each elements
- Add the trainable relative position representations, and add them to key and query vectors

Graph Attention Networks [[Velickovic+, ICLR18](https://arxiv.org/abs/1710.10903)][[#4](https://github.com/InabaTatsuro/papers/issues/4)]
- train weight matrix which represents the relation between nodes
- it can be seen as self attention with artificially created mask

# CV
GibbsDDRM: A Partially Collapsed Gibbs Sampler for Solving Blind Inverse Problems with Denoising Diffusion Restoration [ICML23, [#35](https://github.com/InabaTatsuro/papers/issues/35)]
- solve linear inverse problems using denoising diffusion restoration
- it can be used in cases where the linear operator is unknown

High-Resolution Image Synthesis with Latent Diffusion Models [[Rombach+, CVPR22](https://arxiv.org/abs/2112.10752)]
- LDM performs semactic compression and AE + GAN performs perceptual compression
- the original paper of Stable Diffusion

## Read Later

PeerNets: Exploiting Peer Wisdom Against Adversarial Attacks [[Svoboda+, 18](https://arxiv.org/abs/1806.00088)]
