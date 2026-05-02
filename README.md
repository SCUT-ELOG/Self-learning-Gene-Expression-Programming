# SL-GEP: Self-Learning Gene Expression Programming

This repository contains the source code implementation of SL-GEP (Self-Learning Gene Expression Programming), a evolutionary algorithm for solving symbolic regression problems. The implementation is based on the research paper:

## Paper Reference

Jinghui Zhong, Yaochu Jin, and Weiwei Cai, "Self-learning gene expression programming," IEEE Transactions on Evolutionary Computation, Vol. 20, No. 1, pp. 65-80, February 2016.

## Directory Structure

```
sl-gep-code-dataset/
├── SLGEP.cpp              # Main SL-GEP implementation
├── symbolic regression dataset/  # Benchmark datasets
│   ├── F0_data.txt        # Function 0 dataset (10 runs)
│   ├── F1_data.txt        # Function 1 dataset (10 runs)
│   ├── F2_data.txt        # Function 2 dataset (10 runs)
│   ├── F3_data.txt        # Function 3 dataset (10 runs)
│   ├── tower_data.txt     # Tower function dataset (10 runs)
│   └── Fx_y_training/testing_data.txt  # Training and testing splits for each run
├── README.md              # This file
└── LICENSE                # Apache 2.0 license
```

## Compilation and Execution

### Prerequisites

- C/C++ compiler (GCC, Clang, or MSVC)
- Math library support (usually included with standard compilers)

### Datasets

The dataset includes several benchmark functions:

- **Function 0-3**: Various polynomial and transcendental functions
- **Tower function**: Complex composite function with nested structures

Each function includes 10 independent runs with separate training and testing data.

## Performance Metrics

The algorithm uses Root Mean Squared Error (RMSE) as the primary fitness metric:

```cpp
v = sqrt(v / input_num);  // RMSE calculation
if (v < 1e-4) v = 0;     // Convergence threshold
```

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## Citation

If you use this code in your research, please cite the following paper:

```bibtex
@article{zhong2016self,
  title={Self-learning gene expression programming},
  author={Zhong, Jinghui and Ong, Yaochu and Cai, Weiwei},
  journal={IEEE Transactions on Evolutionary Computation},
  volume={20},
  number={1},
  pages={65--80},
  year={2016},
  publisher={IEEE}
}
```



## References

1. Ferreira, C. (2001). Gene expression programming: A new adaptive algorithm for solving problems. Complex Systems, 13(2), 87-129.
2. Zhong, J., Ong, Y. S., & Cai, W. (2016). Self-learning gene expression programming. IEEE Transactions on Evolutionary Computation, 20(1), 65-80.
3. Koza, J. R. (1992). Genetic programming: On the programming of computers by means of natural selection. MIT Press.
