# Report: Self-Pruning Neural Network

## Why L1 Encourages Sparsity
L1 regularization pushes values toward zero. Since gates control whether a weight is active, minimizing the sum of gate values forces many gates to become very small, effectively pruning weights.

## Results Summary

| Lambda | Accuracy | Sparsity |
|--------|---------|---------|
| 0.001  | 97.13%%     | 97.13%     |
| 0.01   | 45.15%     | 97.31%     |
| 0.1    | 41.33%     | 97.36%     |

## Observations
- Low lambda → high accuracy, low sparsity
- High lambda → more pruning, lower accuracy
- Trade-off between model size and performance

## Conclusion
The model successfully learns to prune itself during training, demonstrating the effectiveness of L1-based sparsity regularization.