# Final report for GSoC 2024 program 


This is the final report for the GSoC 2024 program "Tensor network contraction order optimization and visualization" release by The Julia Language co-mentored by Prof. Jinguo Liu and Prof. Jutho Haegeman.

## Goals of the project

This project aims to further enhance the performance and usability of tensor network tools in Julia. There are three main goals of the project: 
* Extending the optimization methods in OMEinsumContractionOrders.jl with the state of art contraction order optimization algorithms; 
* Implementing a hyper-graph visualization tool for tensor networks as a standalone package;
* Porting the contraction order optimization algorithms in OMEinsumContractionOrders.jl to the TensorOperations.jl package as a backend. 

Testing and documentation will also be done for all implemented methods, and the code will be open-sourced and published to the Julia community.

## Summary of the work

During the GSoC 2024 program, I have successfully implemented the following features:
* I enhance a few existing optimizers in OMEinsumContractionOrders.jl, including the greedy optimizer and the bipartition optimizer.
* I implemented a new Julia package TreeWidthSolver.jl for solving the exact tree width of simple graphs, and used it as an exact optimizer in OMEinsumContractionOrders.jl.
* Based on the LuxorGraphPlots.jl, I implemented a tensor network visualization tool LuxorTensorPlots as an extension of OMEinsumContractionOrders.jl, which can be used to visualize the tensor network as a hyper-graph, and generate videos for the contraction process.
* I ported the contraction order optimization algorithms in OMEinsumContractionOrders.jl to the TensorOperations.jl package as an extension, so that users of TensorOperations.jl can also benefit from the optimizers in OMEinsumContractionOrders.jl.
* Blogs and documentation are written for the implemented methods.

### Current status

Currently, the package [TreeWidthSolver.jl](https://github.com/ArrogantGao/TreeWidthSolver.jl) has been released and can be used as a standalone package. A new version of [OMEinsumContractionOrders.jl](https://github.com/TensorBFS/OMEinsumContractionOrders.jl) has been released with the new optimizers and visualization tools. The porting of the optimizers to TensorOperations.jl is still in progress and will be released soon.

### Links to the repositories and PRs

Links to the repositories are as follows:
* TreeWidthSolver.jl: [https://github.com/ArrogantGao/TreeWidthSolver.jl](https://github.com/ArrogantGao/TreeWidthSolver.jl)
* OMEinsumContractionOrders.jl: [https://github.com/TensorBFS/OMEinsumContractionOrders.jl](https://github.com/TensorBFS/OMEinsumContractionOrders.jl)
* TensorOperations.jl: [https://github.com/Jutho/TensorOperations.jl](https://github.com/Jutho/TensorOperations.jl)
* Benchmark: [https://github.com/ArrogantGao/TreeWidthSolver_benchmark](https://github.com/ArrogantGao/TreeWidthSolver_benchmark)

Important PRs are as follows:
* Enhancement of OMEinsumContractionOrders.jl: [https://github.com/TensorBFS/OMEinsumContractionOrders.jl/pull/41](https://github.com/TensorBFS/OMEinsumContractionOrders.jl/pull/41)
* Tree width based optimizer in OMEinsumContractionOrders.jl: [https://github.com/TensorBFS/OMEinsumContractionOrders.jl/pull/43](https://github.com/TensorBFS/OMEinsumContractionOrders.jl/pull/43), [https://github.com/TensorBFS/OMEinsumContractionOrders.jl/pull/46](https://github.com/TensorBFS/OMEinsumContractionOrders.jl/pull/46)
* LuxorTensorPlots as an extension of OMEinsumContractionOrders.jl: [https://github.com/TensorBFS/OMEinsumContractionOrders.jl/pull/44](https://github.com/TensorBFS/OMEinsumContractionOrders.jl/pull/44)
* The algorithm for solving exact tree width: [https://github.com/ArrogantGao/TreeWidthSolver.jl/pull/8](https://github.com/ArrogantGao/TreeWidthSolver.jl/pull/8)
* A high performance implementation of the graph operations: [https://github.com/ArrogantGao/TreeWidthSolver.jl/pull/14](https://github.com/ArrogantGao/TreeWidthSolver.jl/pull/14)
* Porting the optimizers to TensorOperations.jl: [https://github.com/Jutho/TensorOperations.jl/pull/185](https://github.com/Jutho/TensorOperations.jl/pull/185)

Links to the documentation and blogs are as follows:
* Documentation for TreeWidthSolver.jl: [https://arrogantgao.github.io/TreeWidthSolver.jl/stable/](https://arrogantgao.github.io/TreeWidthSolver.jl/stable/)
* Blog for tensor network contraction order: [https://arrogantgao.github.io/blogs/contractionorder/](https://arrogantgao.github.io/blogs/contractionorder/)
* Blog for solving exact tree width: [https://arrogantgao.github.io/blogs/treewidth/](https://arrogantgao.github.io/blogs/treewidth/)

### Future work

In the future, I will continue to work on the following tasks:
* Finish the porting of the optimizers to TensorOperations.jl and release the new version of TensorOperations.jl.
* Optimize the performance of the TreeWidthSolver.jl package and add more algorithms for solving the tree width of graphs.

## Challenges and learning

During the GSoC program, I have encountered several challenges, including: 
* The implementation of the tree width based optimizer in OMEinsumContractionOrders.jl requires a good understanding of the tree width and the graph theory. I have learned a lot about the tree width and the graph theory during the implementation.
* High performance implementation of the graph operations in TreeWidthSolver.jl requires a good understanding of the Julia language and the performance optimization techniques. I have learned a lot about the performance optimization techniques in Julia during the implementation.

## Acknowledgement

I would like to thank my mentors Prof. Jinguo Liu and Prof. Jutho Haegeman for their guidance and support during the GSoC program. I would also like to thank the Julia community for providing such a great platform for open-source development.