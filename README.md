The included paper describes a structural perturbation method
(SPM) for link prediction/missing links detection that is based on perturbation
of the observed network adjacency matrix. We implement the described algorithm, and test it on the included network.
Specically, we run this algorithm on a provided white-space-separated edge list of the
network, and assign SPM scores to each non-link. We use 10 repetitions
for SPM and choose 10% of existing links as a perturbation set.

We use true missing links specified in a separate file to label all ranked non-
links as true/false positives, and compute the areas under the Receiver
Operator Characteristic (AUROC) and Precision-Recall (AUPR) curves
as the performance scores of the SPM for link prediction in the network.
The code returns these two numbers (areas under ROC
and PR curves), and take as an input the pruned edge list and the list of true
missing links. We use Scikit-Learn for AUROC/AUPR calculations.
