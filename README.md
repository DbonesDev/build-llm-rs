<div align="center">
  <h1>🦀 build-llm-rs</h1>
  
  <p>
    <strong>Deconstructing Large Language Models. Built from scratch in Rust.</strong>
  </p>

  <p>
    <a href="https://github.com/DbonesDev/build-llm-rs/actions">
      <img src="https://img.shields.io/badge/build-passing-brightgreen?style=flat-square&logo=github-actions" alt="Build Status" />
    </a>
    <a href="https://github.com/DbonesDev/build-llm-rs/blob/main/LICENSE">
      <img src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" alt="License" />
    </a>
    <img src="https://img.shields.io/badge/rust-edition%202021-orange?style=flat-square&logo=rust" alt="Rust Edition" />
  </p>

  <p>
    <em>"What I cannot create, I do not understand."</em> — Richard Feynman
  </p>
</div>

<br />
<hr />

## 📖 About The Project

**build-llm-rs** is an engineering laboratory where I implement the architecture of a Large Language Model (GPT-style) entirely in **Rust**.

This project is a code-along adaptation of the excellent book **[Build a Large Language Model (From Scratch)](https://www.manning.com/books/build-a-large-language-model-from-scratch)** by Sebastian Raschka. 

**The Twist:** The book uses Python and PyTorch. **I am porting every concept to Rust.** ### 🎯 The Goal
To demystify the "black box" of AI by forcing myself to understand the mathematics and memory management behind it.
1.  **No Python Magic:** Implementing Tokenizers and Attention mechanisms with strict type safety.
2.  **Bare Metal Performance:** Leveraging Rust's ownership model to manage tensor memory.
3.  **Math over Frameworks:** Understanding the raw matrix multiplications before abstracting them.

---

## 🛠️ The Workbench

* **Language:** Rust 🦀
* **Tensor Backend:** [`Candle`](https://github.com/huggingface/candle) (by Hugging Face) or [`ndarray`](https://github.com/rust-ndarray/ndarray) for raw operations.
* **Serialization:** `Serde`
* **Reference Material:** *Build a Large Language Model (From Scratch)* - Sebastian Raschka.

---

## 🗺️ Progress Log

I am following the book structure, translating concepts chapter by chapter.

| Chapter | Topic | Rust Status | Key Concepts |
| :--- | :--- | :---: | :--- |
| **01** | **Understanding LLMs** | ✅ | *Architecture overview, Transformers history* |
| **02** | **Working with Text** | 🚧 | *Tokenization, BPE, Sliding Window, Data Loaders* |
| **03** | **Coding Attention** | ⏳ | *Self-Attention, Multi-Head Attention, Causal Masks* |
| **04** | **Implementing GPT** | ⏳ | *Layer Normalization, Feed Forward, GELU activation* |
| **05** | **Pretraining** | ⏳ | *Loss functions, Backpropagation loops* |
| **06** | **Finetuning** | ⏳ | *Classification, Instruction Following* |

---

## 🚀 Usage

This is a library/binary hybrid. You can run specific examples or tests corresponding to the chapters.

### Prerequisites
* Rust (Latest Stable)
* Cargo

### Running the implementation
```bash
# Clone the repository
git clone [https://github.com/DbonesDev/build-llm-rs.git](https://github.com/DbonesDev/build-llm-rs.git)
cd build-llm-rs

# Run the main entry point (e.g., Chapter 2 Tokenizer test)
cargo run --bin ch02_tokenizer