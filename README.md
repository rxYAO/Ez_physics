# Ez_physics
Typical algorithms for simulating equilibrium and dynamics of Bose Hubbard Model
This project includes the code written in my BSc and would be quoted in my Bachelor thesis. The guide of this collection is also corresponding to the catalog of thesis.
Basicaly, my focus is quantum many body system. In this field, we apply different algorithm w.r.t. the system size and dimension to solve the problem with balanced accuracy and speed. 
For sites ~ O(1), the best choice would be Exact Diagonalization, for both ground state problem and time evolution. While dimension of Hamiltonian (D) grows, to diagonalize it costs O(D^(3)) but to store it takes only O(D^2). Laptop solves D ~ 10000 in a sparse matrix representation. 
Considering D > 10000 but to construct the Hamiltonian is not unacceptable yet, we apply iterative solver to do real/imagenary time evolution, for example, Krylov propagation and Chebychev propagation.
If D is too large to even store the Hamiltonian matrix, we apply MPS techniques like DMRG (TEBD and TDVP), which takes computational cost at O(D^3) where D refers to bond dimension.
For simulating equilibrium problem reaching thermal limit, one takes Quantum Monte Carlo (sites ~ 100^3). 
