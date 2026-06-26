# RunOnGPU Examples

Example projects for testing and learning RunOnGPU.

This repository contains small projects that can be executed on a free Google Colab GPU using RunOnGPU. The goal is to provide simple, working examples that demonstrate how to configure, build, and run different types of projects.

## Current Examples

### CUDA

* `cuda/vector-add`

  * Basic CUDA vector addition program
  * Demonstrates GPU compilation with `nvcc`
  * Good first project for verifying your RunOnGPU installation

## Getting Started

1. Clone this repository:

```bash
git clone https://github.com/MashrafeeAryan/runongpu-examples.git
```

2. Navigate to an example:

```bash
cd runongpu-examples/cuda/vector-add
```

3. Initialize RunOnGPU:

```bash
runongpu init
```

4. Run the project:

```bash
runongpu run
```

RunOnGPU will:

* Open Google Colab
* Create a notebook copy in your Google Drive (first run only)
* Clone the repository
* Build the project
* Run the project on a GPU-enabled Colab environment

## Repository Structure

```text
runongpu-examples/
├── cuda/
│   └── vector-add/
├── python/
├── pytorch/
└── README.md
```

Additional examples will be added over time, including:

* CUDA
* Python
* PyTorch
* TensorFlow
* CMake projects
* Multi-file C++ projects

## About RunOnGPU

RunOnGPU is a CLI tool that allows developers to execute GPU workloads on free Google Colab GPUs directly from GitHub repositories.

Projects are configured using a simple `runongpu.txt` file:

```text
[setup]

[build]
nvcc main.cu -o vector_add

[test]

[run]
./vector_add
```

The goal is to make GPU experimentation simple, reproducible, and accessible to anyone with a GitHub repository.
