# Linear Clifford Encoder (LCE) and Taylor Surrogate Repository

## Overview

This repository contains the code and notebooks accompanying the academic paper ([arXiv:2507.06344](URL "https://arxiv.org/abs/2507.06344")):

**Trainability of Quantum Models Beyond Known Classical Simulability**  
<u>Sabri Meyer</u>¹, Francesco Scala¹, Francesco Tacchino², and Aurelien Lucchi¹  <br>
¹ Department of Mathematics and Computer Science, University of Basel, 4051 Basel, Switzerland <br>
² IBM Quantum, IBM Research Europe - Zurich, 8803 Rüschlikon, Switzerland

### Abstract
Variational Quantum Algorithms (VQAs) are promising candidates for near-term quantum computing, yet they face scalability challenges due to barren plateaus, where gradients vanish exponentially in the system size. Recent conjectures suggest that avoiding barren plateaus might inherently lead to classical simulability, thus limiting the opportunities for quantum advantage. In this work, we advance the theoretical understanding of the relationship between the trainability and computational complexity of VQAs, thus directly addressing the conjecture. We introduce the Linear Clifford Encoder (LCE), a novel technique that ensures constant-scaling gradient statistics on optimization landscape regions that are close to Clifford circuits. Additionally, we leverage classical Taylor surrogates to reveal computational complexity phase transitions from polynomial to super-polynomial as the initialization region size increases. Combining these results, we reveal a deeper link between trainability and computational complexity, and analytically prove that barren plateaus can be avoided in regions for which no classical surrogate is known to exist. Furthermore, numerical experiments on LCE transformed landscapes confirm in practice the existence of a super-polynomially complex ``transition zone'' where gradients decay polynomially. These findings indicate a plausible path to practically relevant, barren plateau-free variational models with potential for quantum advantage.

---

## Content of the Repository

| File | Description |
|------|--------------|
| `code_LCE-geometry.ipynb` | Experiments studying how LCE changes the geometry of the optimization landscape. |
| `code_VQE.ipynb` | VQE Experiments with exact gradients that compare the training dynamics between models with LCE and without LCE, respectively. |
| `code_VQE_shots.ipynb` | The same experiments as above but with approximated gradients due to finite shots sampling. |
| `code_benchmarking.ipynb` | Benchmarking experiments focusing on classical simulation time with the Taylor surrogate and gradient scalability at $\theta=0$. |
| `code_patchsizes.ipynb` | An additional experiment that computes the hyper-parameters of the parameter initialization for which the Taylor surrogate outperforms the Pauli path surrogate. |
| `code_randomwalk.ipynb` | An additional experiment that shows that GD optimization with LCE is not equivalent to a random walk. |
| `code_trainability.ipynb` | Benchmarking experiments focusing on the gradient scalability across various landscape patches comparing LCE with non-LCE models. |

---
