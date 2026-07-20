# 5.3 Exercises

## Q4

The backward pass itself must be recorded into the computational graph (`create_graph=True`), so the graph grows to forward + backward ($\approx 2\text{-}3\times$ nodes), and second derivatives are obtained by backpropagating through this extended graph — each extra derivative order re-expands the previous graph.

Cost: a Hessian-vector product is only $O(1)\times$ a gradient (Pearlmutter trick), but the full Hessian needs $p$ backward passes and $p^2$ memory — for this section's model ($p \approx 2\times10^5$) that is $\sim165$ GB, already infeasible. Hence practice uses HVPs or block approximations (K-FAC, last-layer Laplace, diagonal/Adam) instead of the explicit Hessian.
