# Deep Learning Course — Complete 20-Lesson Curriculum

Source: [ChatWhole Learn — Deep Learning](https://chatwhole.com/learn/deep-learning/)

---

## Table of Contents

| # | Topic | Link |
|---|-------|------|
| 01 | What Is Deep Learning | [View](https://chatwhole.com/learn/deep-learning/01-what-is-deep-learning/) |
| 02 | Math Foundations for DL | [View](https://chatwhole.com/learn/deep-learning/02-math-foundations-for-dl/) |
| 03 | Backpropagation Algorithm | [View](https://chatwhole.com/learn/deep-learning/03-backpropagation-algorithm/) |
| 04 | Activation Functions | [View](https://chatwhole.com/learn/deep-learning/04-activation-functions/) |
| 05 | Loss Functions for DL | [View](https://chatwhole.com/learn/deep-learning/05-loss-functions-for-dl/) |
| 06 | Optimizers Deep Learning | [View](https://chatwhole.com/learn/deep-learning/06-optimizers-deep-learning/) |
| 07 | Weight Initialization | [View](https://chatwhole.com/learn/deep-learning/07-weight-initialization/) |
| 08 | Regularization Deep Learning | [View](https://chatwhole.com/learn/deep-learning/08-regularization-deep-learning/) |
| 09 | CNN Architecture Deep Dive | [View](https://chatwhole.com/learn/deep-learning/09-cnn-architecture-deep-dive/) |
| 10 | Object Detection | [View](https://chatwhole.com/learn/deep-learning/10-object-detection/) |
| 11 | Semantic Segmentation | [View](https://chatwhole.com/learn/deep-learning/11-semantic-segmentation/) |
| 12 | RNN Deep Dive | [View](https://chatwhole.com/learn/deep-learning/12-rnn-deep-dive/) |
| 13 | LSTM Networks | [View](https://chatwhole.com/learn/deep-learning/13-lstm-networks/) |
| 14 | GRU Networks | [View](https://chatwhole.com/learn/deep-learning/14-gru-networks/) |
| 15 | Sequence to Sequence | [View](https://chatwhole.com/learn/deep-learning/15-sequence-to-sequence/) |
| 16 | Attention Mechanisms Deep Dive | [View](https://chatwhole.com/learn/deep-learning/16-attention-mechanisms-deep-dive/) |
| 17 | Vision Transformers | [View](https://chatwhole.com/learn/deep-learning/17-vision-transformers/) |
| 18 | GANs Deep Dive | [View](https://chatwhole.com/learn/deep-learning/18-gans-deep-dive/) |
| 19 | Variational Autoencoders | [View](https://chatwhole.com/learn/deep-learning/19-variational-autoencoders/) |
| 20 | Diffusion Models Deep Dive | [View](https://chatwhole.com/learn/deep-learning/20-diffusion-models-deep-dive/) |

---

## 01 — What Is Deep Learning

**Link:** https://chatwhole.com/learn/deep-learning/01-what-is-deep-learning/

### Key Concepts

- **Hierarchical Feature Learning** — Networks automatically discover features from raw data
- **Depth Equals Efficiency** — Deeper networks represent complex functions with exponentially fewer parameters
- **Modern Revolution** — Big data, GPUs, and algorithmic advances converged to make deep learning practical

### Deep Learning vs Traditional Machine Learning

| Aspect | Traditional ML | Deep Learning |
|--------|---------------|---------------|
| Feature Engineering | Manual | Automatic |
| Input | Hand-crafted features | Raw data (pixels, text, audio) |
| Learning | Limited by features | Learns feature hierarchy |

### Timeline of Deep Learning

| Year | Milestone | Key Innovation |
|------|-----------|----------------|
| 1958 | Perceptron | Linear classifiers |
| 1969 | AI Winter | Minsky proves XOR limitation |
| 1986 | Backprop | Multi-layer networks |
| 2012 | AlexNet | Won ImageNet, proved deep CNNs work |
| 2015 | ResNet | Skip connections, 152 layers |
| 2017 | Transformer | Self-attention, replaced RNNs for NLP |
| 2020 | GPT-3 | Large language models (175B params) |
| 2022 | Stable Diffusion | Generative AI breakthrough |
| 2023 | GPT-4 / LLaMA | Multimodal, open-source LLMs |

### When to Use Deep Learning

Use deep learning when:
- Data is unstructured (images, video, audio, text)
- Large datasets (>10K samples)
- Complex patterns exist
- GPU is available

### Three Pillars of Deep Learning

1. Big data availability
2. GPU computing power
3. Algorithmic advances (ReLU, dropout, batch norm, skip connections)

---

## 02 — Math Foundations for DL

**Link:** https://chatwhole.com/learn/deep-learning/02-math-foundations-for-dl/

### Linear Algebra

**Vectors and Matrices** — Building blocks of all neural network operations.

**Matrix Operations in Neural Networks:**
```
z = Wx + b
```
Where:
- x = input vector
- W = weight matrix
- b = bias vector
- z = output vector

**Eigenvalues and Eigenvectors:**
- Used in PCA, spectral clustering, and understanding matrix transformations

**Singular Value Decomposition (SVD):**
```
A = U × Σ × V^T
```
- U = orthogonal (left singular vectors)
- Σ = diagonal (singular values)
- V^T = orthogonal (right singular vectors)

### Calculus for Deep Learning

**The Chain Rule:**
```
∂z/∂x = (∂z/∂y) · (∂y/∂x)
```
- Backbone of backpropagation
- Enables efficient gradient computation through layers

**Jacobian and Hessian:**
- Jacobian: matrix of first derivatives
- Hessian: matrix of second derivatives
- Used in optimization and second-order methods

### Probability Theory

**Key Distributions in Deep Learning:**

| Distribution | Use Case |
|-------------|----------|
| Gaussian | Weight init, VAE, Diffusion |
| Bernoulli | Dropout, binary classification |
| Categorical | Classification, Softmax |

**Information Theory:**
- Cross-entropy loss
- KL divergence for regularization
- Entropy for uncertainty measurement

### Practical Applications

| Math Concept | DL Application |
|-------------|----------------|
| Matrix multiplication | Forward pass |
| Chain rule | Backpropagation |
| Eigendecomposition | PCA, weight analysis |
| Gaussian distributions | Weight initialization, VAE |
| KL divergence | Regularization, knowledge distillation |

---

## 03 — Backpropagation Algorithm

**Link:** https://chatwhole.com/learn/deep-learning/03-backpropagation-algorithm/

### What Is Backpropagation?

The algorithm that enables neural networks to learn from data. It efficiently computes the gradient of the loss with respect to every parameter using the chain rule.

### Computational Graphs

```
f(x,y) = (x+y)·(x·y)

Forward Pass:
a = x + b
b = x · y
f = a · b

Backward Pass:
∂f/∂f = 1
∂f/∂a = b
∂f/∂b = a
∂f/∂x = b + a
∂f/∂y = b + a
```

### Forward Pass

```
Input → h⁰ = x
Layer 1: z¹ = W¹h⁰ + b¹, h¹ = σ(z¹)
Layer 2: z² = W²h¹ + b², h² = σ(z²)
Layer 3: z³ = W³h² + b³, h³ = σ(z³)
Output: ŷ
```

### Backward Pass

```
∂L/∂h³ = 1
∂L/∂z³ = ∂L/∂h³ · σ'(z³)
∂L/∂W³ = ∂L/∂z³ · (h²)ᵀ
∂L/∂z² = ∂L/∂h² · σ'(z²)
∂L/∂W² = ∂L/∂z² · (h¹)ᵀ
```

**General formula:**
```
∂L/∂W⁽ˡ⁾ = ∂L/∂z⁽ˡ⁾ · (h⁽ˡ⁻¹⁾)ᵀ
```

### Vanishing/Exploding Gradients

| Problem | Cause | Solution |
|---------|-------|----------|
| Vanishing | Sigmoid, tanh, small init | ReLU, skip connections |
| Exploding | Large weights | Gradient clipping |

### PyTorch Autograd

```python
import torch
x = torch.tensor(2.0, requires_grad=True)
y = x ** 2
y.backward()
print(x.grad)  # 4.0
```

---

## 04 — Activation Functions

**Link:** https://chatwhole.com/learn/deep-learning/04-activation-functions/

### Why Activation Functions?

Without activation functions, deep networks collapse into linear models:
```
W₃ · W₂ · W₁ · x = W' · x (equivalent to single layer)
```

### Activation Function Comparison

| Function | Formula | Range | Use Case |
|----------|---------|-------|----------|
| Sigmoid | 1/(1+e^(-x)) | (0,1) | Binary output |
| Tanh | (e^x-e^(-x))/(e^x+e^(-x)) | (-1,1) | Hidden layers |
| ReLU | max(0,x) | [0,∞) | Default hidden |
| Leaky ReLU | max(αx,x) | (-∞,∞) | Avoid dead neurons |
| GELU | x·Φ(x) | (-∞,∞) | Transformers |
| Swish | x·σ(x) | (-∞,∞) | Deep networks |

### ReLU and Variants

- **ReLU**: Fast, prevents vanishing gradients, sparse activations
- **Leaky ReLU**: Allows small negative values, prevents dead neurons
- **PReLU**: Learned negative slope

### GELU and Swish

Modern activation functions used in transformers:
- **GELU**: Smooth ReLU approximation, used in BERT, GPT, ViT
- **Swish**: Self-gated, smooth, used in EfficientNet

### Softmax

For multi-class output:
```
softmax(zᵢ) = e^(zᵢ) / Σⱼ e^(zⱼ)
```

### When to Use Each

| Layer Type | Recommended Activation |
|-----------|----------------------|
| Hidden layers | ReLU (default), GELU (transformers) |
| Output (multi-class) | Softmax |
| Output (binary) | Sigmoid |
| Output (regression) | None |

### The Dead Neuron Problem

ReLU neurons that always output zero:
- Caused by large negative pre-activations
- Solution: Leaky ReLU, careful initialization, lower learning rate

---

## 05 — Loss Functions for DL

**Link:** https://chatwhole.com/learn/deep-learning/05-loss-functions-for-dl/

### Loss Function Taxonomy

```
Task Type?
├── Regression → MSE / MAE / Huber
├── Classification → Cross-Entropy / Focal
└── Ranking/Similarity → Triplet / Contrastive
```

### Mean Squared Error (MSE)

```
L = (ŷ - y)²
∂L/∂ŷ = 2(ŷ - y)
```
- Quadratic penalty, sensitive to outliers
- Used for regression tasks

### Cross-Entropy Loss

**Binary:**
```
L = -[y·log(ŷ) + (1-y)·log(1-ŷ)]
```

**Multi-class:**
```
L = -Σᵢ yᵢ·log(ŷᵢ)
```
- Equivalent to maximum likelihood estimation
- Standard for classification

### Focal Loss

```
FL(pₜ) = -αₜ(1-pₜ)^γ · log(pₜ)
```
- Down-weights easy examples
- Focuses on hard, rare cases
- Default γ=2

### Huber Loss

Combines MSE and MAE:
```
Lδ(a) = { ½a²           if |a| ≤ δ
        { δ(|a| - ½δ)   otherwise
```
- Robust to outliers
- Smooth transition between MSE and MAE

### Contrastive and Triplet Loss

- **Triplet loss**: anchor, positive, negative
- **Contrastive loss**: same/different pairs
- Used for learning embeddings

### Label Smoothing

```
y_smooth = (1-ε)·y + ε/K
```
- Prevents overconfident predictions
- Improves generalization

---

## 06 — Optimizers Deep Learning

**Link:** https://chatwhole.com/learn/deep-learning/06-optimizers-deep-learning/

### Gradient Descent Foundation

```
θ = θ - η · ∇L(θ)
```

### SGD with Momentum

```
v = β·v + η·∇L(θ)
θ = θ - v
```
- β typically 0.9
- Smooths noisy gradients
- Faster convergence than vanilla SGD

### Adam

```
m = β₁·m + (1-β₁)·∇L(θ)        # First moment
v = β₂·v + (1-β₂)·(∇L(θ))²     # Second moment
m̂ = m/(1-β₁ᵗ)                    # Bias correction
v̂ = v/(1-β₂ᵗ)                    # Bias correction
θ = θ - η·m̂/(√v̂ + ε)
```
Default: β₁=0.9, β₂=0.999, ε=1e-8

### AdamW

Adam with decoupled weight decay:
```
θ = θ - η·(m̂/(√v̂ + ε) + λ·θ)
```

### Learning Rate Schedules

**Cosine Annealing:**
```
η(t) = η_min + ½(η_max - η_min)(1 + cos(πt/T))
```

**Warmup:**
- Linear warmup for first few epochs
- Prevents early instability

### Optimizer Selection

| Task | Optimizer | Learning Rate |
|------|-----------|---------------|
| NLP/Transformers | AdamW | 2e-5 |
| Computer Vision | SGD+Momentum | 0.1 |
| GANs/RL | Adam | 1e-4 |

---

## 07 — Weight Initialization

**Link:** https://chatwhole.com/learn/deep-learning/07-weight-initialization/

### Why Initialization Matters

Poor initialization causes vanishing/exploding gradients before training begins.

### Xavier/Glorot Initialization

For sigmoid/tanh activations:
```
W ~ N(0, 2/(n_in + n_out))
W ~ U(-√(6/(n_in+n_out)), √(6/(n_in+n_out)))
```
Preserves variance across layers.

### He/Kaiming Initialization

For ReLU activations:
```
W ~ N(0, 2/n_in)
W ~ N(0, √(2/n_in))
```
Doubles variance to compensate for ReLU zeroing half the activations.

### Orthogonal Initialization

- Preserves gradient magnitude through time
- Used for RNNs/LSTMs

### LSUV (Layer-sequential Unit-Variance)

- Data-driven initialization
- Works for any architecture
- Normalizes activations to unit variance

### ResNet Zero-Init Trick

Initialize last batch norm to zero in residual blocks:
- Ensures identity mapping at initialization
- Enables training of very deep networks

### Initialization Recommendations

| Architecture | Recommended Initialization |
|-------------|--------------------------|
| CNNs | He (Kaiming) + ReLU |
| ResNets | He + zero-init BN |
| Transformers | Xavier for embeddings, 1/√d for projections |
| RNNs/LSTMs | Orthogonal recurrent, Xavier input→hidden |

---

## 08 — Regularization Deep Learning

**Link:** https://chatwhole.com/learn/deep-learning/08-regularization-deep-learning/

### The Overfitting Problem

Deep networks have far more parameters than training samples, making them prone to overfitting.

### Dropout

- Randomly zeros neurons during training (p=0.5 typical)
- Acts as implicit ensemble of subnetworks
- At inference: scale by 1/(1-p)

```python
nn.Dropout(p=0.5)  # 50% dropout rate
```

### Batch Normalization

Normalizes across batch dimension:
```
x̂ = (x - μ_B) / √(σ²_B + ε)
y = γx̂ + β
```
- Allows 10-100x higher learning rates
- Stabilizes training

### Layer Normalization

Normalizes across feature dimension:
```
x̂ = (x - μ) / √(σ² + ε)
```
- Preferred for transformers/NLP
- No dependency on batch size

### Weight Decay

L2 regularization:
```
θ = θ - η(∇L + λθ)
```
- λ typically 0.01-0.1
- Always use with proper value

### Data Augmentation

Increases effective training set size:
- Flips, rotations, crops (images)
- Synonym replacement, back-translation (text)
- Mixup, CutMix

### Early Stopping

Monitor validation loss; stop when it starts increasing.

### Regularization Comparison

| Technique | Mechanism | When to Use |
|-----------|-----------|-------------|
| Dropout | Random neuron removal | FC layers, transformers |
| BatchNorm | Normalize activations | CNNs |
| LayerNorm | Normalize per sample | Transformers |
| Weight Decay | Penalize large weights | Always |
| Data Augment | Increase data diversity | CV tasks |
| Early Stopping | Stop when val loss rises | Always |

---

## 09 — CNN Architecture Deep Dive

**Link:** https://chatwhole.com/learn/deep-learning/09-cnn-architecture-deep-dive/

### The Convolution Operation

```
Output(i,j) = Σ Input(i+m, j+n) × Kernel(m, n)
```

Each output = dot product of kernel with local region.

### Padding and Stride

- **Same padding**: output size = input size
- **Valid padding**: no padding
- **Stride**: step size for kernel movement

### Pooling

- **Max pooling**: takes maximum value in window
- **Average pooling**: takes average value
- Reduces spatial dimensions

### CNN Architecture Evolution

| Year | Architecture | Key Innovation |
|------|-------------|----------------|
| 1998 | LeNet | First practical CNN |
| 2012 | AlexNet | ReLU, dropout, GPU training |
| 2014 | VGGNet | Uniform 3×3 filters |
| 2014 | GoogLeNet | Inception modules |
| 2015 | ResNet | Skip connections, 152 layers |
| 2019 | EfficientNet | Compound scaling |

### ResNet Skip Connection

```
y = F(x) + x
```
- Enables gradient flow through skip connections
- Enables training of 100+ layer networks

### Inception Module

Multi-scale feature extraction with parallel branches:
- 1×1 conv
- 3×3 conv
- 5×5 conv
- 3×3 max pool

### Depthwise Separable Convolution

Factorizes standard convolution into:
1. Depthwise convolution (spatial)
2. Pointwise convolution (1×1)

Used in MobileNet, EfficientNet.

---

## 10 — Object Detection

**Link:** https://chatwhole.com/learn/deep-learning/10-object-detection/

### Detection vs Classification

Object detection predicts:
1. Bounding boxes
2. Class labels
3. Confidence scores

### IoU (Intersection over Union)

```
IoU = Intersection / Union
```
- IoU > 0.5: acceptable
- IoU > 0.7: good
- IoU > 0.9: excellent

### Anchor Boxes

Reference shapes for bounding box regression.

### Non-Maximum Suppression (NMS)

Removes duplicate detections by keeping highest confidence boxes.

### Two-Stage: Faster R-CNN

1. Region Proposal Network (RPN)
2. Classification + Box Regression

- Higher accuracy
- Slower (2-5 FPS)

### Single-Stage: YOLO

- Grid-based prediction
- Real-time (30+ FPS)
- YOLOv8: state-of-the-art speed/accuracy

### Two-Stage vs Single-Stage

| Aspect | Two-Stage | Single-Stage |
|--------|-----------|--------------|
| Accuracy | Higher mAP | Lower mAP |
| Speed | 2-5 FPS | 30+ FPS |
| Small objects | Better | Worse |
| Examples | Faster R-CNN, Mask R-CNN | YOLO, SSD, RetinaNet |

### Evaluation: mAP

Mean Average Precision over IoU thresholds.

---

## 11 — Semantic Segmentation

**Link:** https://chatwhole.com/learn/deep-learning/11-semantic-segmentation/

### Segmentation Types

| Type | Description |
|------|-------------|
| Semantic | All instances of same class have same label |
| Instance | Each instance gets unique label |
| Panoptic | Combines semantic + instance |

### Fully Convolutional Network (FCN)

- Replaces fully connected layers with convolutions
- Enables pixel-wise prediction

### U-Net Architecture

Encoder-decoder with skip connections:
- **Encoder**: downsampling path
- **Decoder**: upsampling path
- **Skip connections**: concatenate encoder features

Dominates medical imaging.

### DeepLab

- Atrous (dilated) convolution for larger receptive field
- ASPP: multi-scale feature extraction
- Fast and accurate

### Loss Functions for Segmentation

- **Dice loss**: overlap-based
- **BCE**: pixel-wise binary cross-entropy
- **Dice + BCE**: standard combination

### Evaluation: mIoU

Mean Intersection over Union across all classes.

### Applications

| Domain | Application |
|--------|-------------|
| Medical Imaging | Tumor segmentation, organ delineation |
| Autonomous Driving | Road, lane, pedestrian detection |
| Satellite | Land use mapping |
| Industrial | Defect detection |

---

## 12 — RNN Deep Dive

**Link:** https://chatwhole.com/learn/deep-learning/12-rnn-deep-dive/

### Why Recurrence?

Process sequential data by maintaining a hidden state.

### Vanilla RNN

```
h_t = tanh(W_hh · h_{t-1} + W_xh · x_t + b)
```

Same parameters shared across all time steps.

### Backpropagation Through Time (BPTT)

Unrolls the RNN and applies backpropagation through the unrolled graph.

### Vanishing and Exploding Gradients

| Problem | Time Steps | Solution |
|---------|-----------|----------|
| Vanishing | ~10-20 | LSTM, GRU, skip connections |
| Exploding | Any | Gradient clipping |

### Solutions

- LSTM/GRU (gating)
- Orthogonal initialization
- Skip connections
- Gradient clipping

### Applications

- Language modeling
- Speech recognition
- Time series forecasting
- Music generation

---

## 13 — LSTM Networks

**Link:** https://chatwhole.com/learn/deep-learning/13-lstm-networks/

### Why LSTMs?

Solve vanishing gradient problem of vanilla RNNs using gating mechanisms.

### LSTM Cell Architecture

**Cell State (c_t)** — Information Highway:
```
c_t = f_t ⊙ c_{t-1} + i_t ⊙ c̃_t
```

**Three Gates:**

1. **Forget Gate:**
   ```
   f_t = σ(W_f · [h_{t-1}, x_t])
   ```

2. **Input Gate:**
   ```
   i_t = σ(W_i · [h_{t-1}, x_t])
   ```

3. **Output Gate:**
   ```
   o_t = σ(W_o · [h_{t-1}, x_t])
   ```

**Cell Candidate:**
```
c̃_t = tanh(W_c · [h_{t-1}, x_t])
```

**Hidden State:**
```
h_t = o_t ⊙ tanh(c_t)
```

### Why LSTMs Solve Vanishing Gradients

Cell state update is linear:
```
c_t = f_t ⊙ c_{t-1} + i_t ⊙ c̃_t
```
Gradients flow through addition → preserved across time steps.

### Bidirectional LSTM

- Processes sequence in both directions
- Captures past and future context
- Concatenates forward and backward hidden states

### Stacked LSTM

- Multiple LSTM layers
- Each layer's output feeds the next
- Captures hierarchical patterns

### LSTM vs GRU

| Feature | LSTM | GRU |
|---------|------|-----|
| Gates | 3 | 2 |
| Cell state | Yes | No |
| Parameters | More | Fewer |
| Speed | Slower | Faster |
| Performance | Similar | Similar |

---

## 14 — GRU Networks

**Link:** https://chatwhole.com/learn/deep-learning/14-gru-networks/

### Why GRU?

Simpler alternative to LSTM with comparable performance.

### GRU Cell Architecture

**Update Gate (z_t):**
```
z_t = σ(W_z · [h_{t-1}, x_t])
```

**Reset Gate (r_t):**
```
r_t = σ(W_r · [h_{t-1}, x_t])
```

**Candidate:**
```
h̃_t = tanh(W · [r_t ⊙ h_{t-1}, x_t])
```

**Interpolation:**
```
h_t = (1-z_t) ⊙ h_{t-1} + z_t ⊙ h̃_t
```

Convex combination of old state and candidate.

### GRU vs LSTM

| Feature | GRU | LSTM |
|---------|-----|------|
| Gates | 2 | 3 |
| States | Hidden only | Hidden + Cell |
| Parameters | Fewer | More |
| Training speed | Faster | Slower |
| Performance | Comparable | Comparable |

---

## 15 — Sequence to Sequence

**Link:** https://chatwhole.com/learn/deep-learning/15-sequence-to-sequence/

### Encoder-Decoder Architecture

Maps variable-length input to variable-length output:
1. **Encoder**: processes input sequence
2. **Decoder**: generates output sequence

### Context Vector

```
c = h_T (final encoder hidden state)
```
Information bottleneck: entire input compressed into single vector.

### Teacher Forcing

- Feed ground truth as input during training
- Stabilizes training
- Introduces exposure bias

### Decoding Strategies

**Greedy Decoding:**
- Choose highest probability token at each step
- Fast but may miss global optimum

**Beam Search:**
- Keep top-k candidates at each step
- Better quality, more compute

### Applications

- Machine translation
- Text summarization
- Dialogue systems
- Code generation

---

## 16 — Attention Mechanisms Deep Dive

**Link:** https://chatwhole.com/learn/deep-learning/16-attention-mechanisms-deep-dive/

### Why Attention?

Solves the information bottleneck in seq2seq models by allowing decoder to "look at" all encoder states.

### Bahdanau Attention

```
e_{i,j} = a(s_{i-1}, h_j)
α_{i,j} = softmax(e_{i,j})
c_i = Σ_j α_{i,j} · h_j
```

### Luong Attention

| Type | Score Function |
|------|---------------|
| Dot | s^T · h |
| General | s^T · W · h |
| Concat | v^T · tanh(W[s;h]) |

### Self-Attention

```
Attention(Q, K, V) = softmax(QK^T / √d_k) · V
```

- Q = queries, K = keys, V = values
- √d_k scaling prevents large dot products

### Multi-Head Attention

```python
MultiHead(Q, K, V) = Concat(head_1, ..., head_h) · W_O
where head_i = Attention(QW_Q^i, KW_K^i, VW_V^i)
```

Captures different types of relationships simultaneously.

### Attention Patterns

- Local attention: focuses on nearby positions
- Global attention: attends to all positions
- Sparse attention: attends to subset of positions

---

## 17 — Vision Transformers

**Link:** https://chatwhole.com/learn/deep-learning/17-vision-transformers/

### From NLP to Vision

Apply Transformer to images by treating patches as tokens.

### Patch Embedding

```
# 224×224 image, patch size 16
# 196 patches of 16×16
# Each patch flattened to 768 dimensions
```

### ViT Architecture

1. **Patch Embedding**: Conv2d(16, 16)
2. **[CLS] Token**: prepended for classification
3. **Positional Embedding**: learnable
4. **Transformer Encoder**: L=12 layers
5. **Classification Head**: Linear(768, 1000)

### ViT vs CNN

| Aspect | CNN | ViT |
|--------|-----|-----|
| Inductive bias | Local connectivity | None (global attention) |
| Data requirement | Works with less data | Needs large dataset |
| Computational cost | O(k²·n) | O(n²) |
| Position info | Built-in | Explicit encoding |

### DeiT (Data-efficient Image Transformers)

- Knowledge distillation
- Strong data augmentation
- Competitive with less data

### Swin Transformer

- Shifted window attention
- Linear complexity
- Hierarchical representation

---

## 18 — GANs Deep Dive

**Link:** https://chatwhole.com/learn/deep-learning/18-gans-deep-dive/

### The GAN Framework

Two neural networks in minimax game:

**Generator (G):**
```
min_G max_D V(D,G) = E[log D(x)] + E[log(1-D(G(z)))]
```

**Discriminator (D):**
- Classifies real vs fake
- Outputs probability

**Nash Equilibrium:**
- p_G = p_data
- D(x) = 0.5 for all x

### DCGAN (Deep Convolutional GAN)

- Transposed convolutions for upsampling
- Batch normalization
- Stable training guidelines

### WGAN (Wasserstein GAN)

- Wasserstein distance instead of JS divergence
- Gradient penalty for stability
- Better training convergence

### StyleGAN

- Style-based generator
- Adaptive instance normalization
- Style mixing at different layers

### Training Challenges

| Challenge | Description | Solution |
|-----------|-------------|----------|
| Mode collapse | Generator produces limited variety | Minibatch discrimination |
| Training instability | Oscillating losses | WGAN, spectral normalization |
| Vanishing gradients | D too strong | Label smoothing, training ratio |

### Evaluation

- **FID (Fréchet Inception Distance)**: standard metric
- **IS (Inception Score)**: diversity and quality

---

## 19 — Variational Autoencoders

**Link:** https://chatwhole.com/learn/deep-learning/19-variational-autoencoders/

### From Autoencoder to VAE

Standard autoencoder: encodes to fixed point
VAE: encodes to probability distribution

### VAE Architecture

1. **Encoder**: q_φ(z|x) → μ, σ²
2. **Reparameterization**: z = μ + σ ⊙ ε
3. **Decoder**: p_θ(x|z) → x̂
4. **Loss**: Reconstruction + KL

### Evidence Lower Bound (ELBO)

```
ELBO = E[log p_θ(x|z)] - D_KL(q_φ(z|x) || p(z))
```

- First term: reconstruction quality
- Second term: latent space regularization

### Reparameterization Trick

```
z = μ + σ ⊙ ε, where ε ~ N(0,1)
```

Makes sampling differentiable → enables end-to-end training.

### Beta-VAE

```
ELBO = E[log p_θ(x|z)] - β · D_KL(q_φ(z|x) || p(z))
```
- β > 1: more disentangled representations
- β < 1: better reconstruction

### VQ-VAE

- Discrete latent space
- Vector quantization
- Used for high-quality generation

---

## 20 — Diffusion Models Deep Dive

**Link:** https://chatwhole.com/learn/deep-learning/20-diffusion-models-deep-dive/

### Forward Process (Diffusion)

Gradually add noise to data:
```
q(x_t|x_{t-1}) = N(x_t; √(1-β_t)·x_{t-1}, β_t·I)
```

### Reverse Process

Learn to denoise step by step:
```
p_θ(x_{t-1}|x_t) = N(x_{t-1}; μ_θ(x_t,t), Σ_θ(x_t,t))
```

### DDPM (Denoising Diffusion Probabilistic Models)

**Training objective:**
```
L = E[||ε - ε_θ(x_t, t)||²]
```
Simple noise prediction loss.

### Key Innovations

| Innovation | Description |
|-----------|-------------|
| Classifier-free guidance | Control generation without classifier |
| Latent diffusion | Work in latent space for efficiency |
| Text conditioning | CLIP embeddings for text-to-image |

### Diffusion vs GANs

| Aspect | Diffusion | GANs |
|--------|-----------|------|
| Quality | Higher FID | Lower FID |
| Diversity | Better | Mode collapse risk |
| Training | Stable | Unstable |
| Speed | Slower (many steps) | Faster (single pass) |

### Applications

- Text-to-image (Stable Diffusion, DALL-E)
- Image inpainting
- Super resolution
- Video generation
- 3D generation

---

## Additional Resources

- **Full Course:** https://chatwhole.com/learn/deep-learning/
- **Statistics:** https://chatwhole.com/learn/statistics/
- **Machine Learning:** https://chatwhole.com/learn/machine-learning/
- **Python:** https://chatwhole.com/learn/python/
- **Data Science:** https://chatwhole.com/learn/data-science/
- **LLM:** https://chatwhole.com/learn/llm/
- **Generative AI:** https://chatwhole.com/learn/generative-ai/
- **NLP:** https://chatwhole.com/learn/nlp/

---

*Source: ChatWhole Learn — Free Deep Learning Tutorials*
