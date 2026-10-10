# 🧠 Deep Learning

<p align="center">
  <img src="deep-learning-cheat-sheet.svg" alt="Deep Learning Cheat Sheet" width="100%">
</p>

## 📚 Table of Contents

1. [Neural Networks](#neural-networks)
2. [Activation Functions](#activation-functions)
3. [CNN Architectures](#cnn-architectures)
4. [RNN & LSTM](#rnn--lstm)
5. [Transformers](#transformers)

---

## 🔗 Neural Networks

### Basic Architecture

```
Input Layer → Hidden Layer(s) → Output Layer
```

### Key Concepts

| Concept | Description |
|---------|-------------|
| **Neuron** | Basic unit, computes weighted sum + bias |
| **Weights** | Parameters learned during training |
| **Bias** | Shifts activation function |
| **Loss Function** | Measures prediction error |
| **Optimizer** | Updates weights to minimize loss |

### Forward Propagation

```
z = Σ(wᵢxᵢ) + b
a = activation(z)
```

### Backpropagation

```
∂Loss/∂w = ∂Loss/∂a * ∂a/∂z * ∂z/∂w
```

---

## ⚡ Activation Functions

| Function | Formula | Range | Use Case |
|----------|---------|-------|----------|
| **Sigmoid** | 1/(1+e⁻ˣ) | (0,1) | Binary output |
| **Tanh** | (eˣ-e⁻ˣ)/(eˣ+e⁻ˣ) | (-1,1) | Hidden layers |
| **ReLU** | max(0,x) | [0,∞) | Default choice |
| **Leaky ReLU** | max(0.01x,x) | (-∞,∞) | Dying ReLU problem |
| **Softmax** | eˣᵢ/Σeˣⱼ | (0,1) sum=1 | Multi-class output |

---

## 🖼️ CNN Architectures

### Architecture Comparison

| Architecture | Layers | Parameters | Year | Key Innovation |
|--------------|--------|------------|------|----------------|
| **LeNet-5** | 7 | 60K | 1998 | First CNN |
| **AlexNet** | 8 | 60M | 2012 | ReLU, Dropout |
| **VGG-16** | 16 | 138M | 2014 | 3x3 filters |
| **GoogLeNet** | 22 | 6.8M | 2014 | Inception modules |
| **ResNet-50** | 50 | 25.6M | 2015 | Skip connections |
| **EfficientNet** | - | 5.3M | 2019 | Compound scaling |

### CNN Building Blocks

```python
# Convolutional Layer
Conv2D(filters, kernel_size, activation='relu')

# Pooling Layer
MaxPooling2D(pool_size=(2,2))

# Flatten Layer
Flatten()

# Dense Layer
Dense(units, activation='softmax')
```

---

## 🔄 RNN & LSTM

### RNN Types

| Type | Architecture | Use Case |
|------|--------------|----------|
| **Vanilla RNN** | One-to-one | Simple sequences |
| **Many-to-One** | Sequence → Single | Sentiment analysis |
| **One-to-Many** | Single → Sequence | Image captioning |
| **Many-to-Many** | Sequence → Sequence | Machine translation |

### LSTM Architecture

```
Cell State: Cₜ = fₜ * Cₜ₋₁ + iₜ * C̃ₜ
Hidden State: hₜ = oₜ * tanh(Cₜ)

Forget Gate: fₜ = σ(Wf · [hₜ₋₁, xₜ] + bf)
Input Gate: iₜ = σ(Wi · [hₜ₋₁, xₜ] + bi)
Output Gate: oₜ = σ(Wo · [hₜ₋₁, xₜ] + bo)
```

---

## 🤖 Transformers

### Attention Mechanism

```
Attention(Q,K,V) = softmax(QKᵀ/√dₖ)V
```

### Transformer Architecture

| Component | Function |
|-----------|----------|
| **Multi-Head Attention** | Parallel attention computation |
| **Positional Encoding** | Add position information |
| **Feed-Forward Network** | Non-linear transformation |
| **Layer Normalization** | Stabilize training |

### Popular Models

| Model | Year | Parameters | Use Case |
|-------|------|------------|----------|
| **BERT** | 2018 | 340M | NLU tasks |
| **GPT-2** | 2019 | 1.5B | Text generation |
| **T5** | 2020 | 11B | Text-to-text |
| **GPT-3** | 2020 | 175B | Few-shot learning |
| **GPT-4** | 2023 | ~1.7T | Multimodal |

---

## 🔗 Related Resources

| Resource | Link |
|----------|------|
| 🧠 Deep Learning Tutorial | [ChatWhole.com/learn/deep-learning](https://chatwhole.com/learn/deep-learning/) |
| 🤖 Machine Learning | [ChatWhole.com/learn/machine-learning](https://chatwhole.com/learn/machine-learning/) |
| 🐍 Python for DL | [ChatWhole.com/learn/python](https://chatwhole.com/learn/python/) |
| 🤖 ML: Neural Networks | [ChatWhole.com/learn/machine-learning/21-neural-networks](https://chatwhole.com/learn/machine-learning/21-neural-networks/) |
| 🤖 ML: Transformers | [ChatWhole.com/learn/machine-learning/25-transformers](https://chatwhole.com/learn/machine-learning/25-transformers/) |
| ✨ Generative AI: Introduction | [ChatWhole.com/learn/generative-ai/01-introduction-to-generative-ai](https://chatwhole.com/learn/generative-ai/01-introduction-to-generative-ai/) |
| ✨ Generative AI: Diffusion Models | [ChatWhole.com/learn/generative-ai/02-diffusion-models](https://chatwhole.com/learn/generative-ai/02-diffusion-models/) |
| 🧠 LLM: What Are Large Language Models | [ChatWhole.com/learn/llm/01-what-are-large-language-models](https://chatwhole.com/learn/llm/01-what-are-large-language-models/) |
| 🧠 LLM: LLM Architecture Deep Dive | [ChatWhole.com/learn/llm/02-llm-architecture-deep-dive](https://chatwhole.com/learn/llm/02-llm-architecture-deep-dive/) |
| 🤖 AI Agents: Building Your First Agent | [ChatWhole.com/learn/ai-agents/01-building-your-first-agent](https://chatwhole.com/learn/ai-agents/01-building-your-first-agent/) |
| 🏗️ AI System Design: LLM System Design | [ChatWhole.com/learn/ai-system-design/12-llm-system-design](https://chatwhole.com/learn/ai-system-design/12-llm-system-design/) |
| 📡 Kafka: Security | [ChatWhole.com/learn/kafka/07-kafka-security](https://chatwhole.com/learn/kafka/07-kafka-security/) |
| 📡 Kafka: Multi-Datacenter | [ChatWhole.com/learn/kafka/08-kafka-multi-datacenter](https://chatwhole.com/learn/kafka/08-kafka-multi-datacenter/) |
| ✨ Generative AI Hub | [generative-ai/README.md](../generative-ai/README.md) |
| 🧠 LLM Hub | [llm/README.md](../llm/README.md) |
| 🤖 AI Agents Hub | [ai-agents/README.md](../ai-agents/README.md) |
| 🏥 Healthcare AI (imaging DL) | [healthcare-ai/README.md](../healthcare-ai/README.md) |
| 🛸 Drone AI (vision DL) | [drone-ai/README.md](../drone-ai/README.md) |
| 🔬 Quantum ML | [quantum-computing/README.md](../quantum-computing/README.md) |

---

<p align="center">
  <a href="https://chatwhole.com">← Back to ChatWhole.com</a>
</p>
