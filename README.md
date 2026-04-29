# NAS (Neural Architecture Search)

### what is NAS and motivation?

motivation can be explained by an example situation:
- "you are a medical expert and wants to design a model, but all the top models are designed by AI masters (some people that are the CR7 of AI). so you are not an AI expert, so how can you choose the best model to help you to deal with your cancer pacients and all the shit you have to deal?" 
- the solution for this problem is the search algorithm called NAS (woooow)

### overview of search methods

- reinforcement learning (cycle: begin -> RNN generates sample architecture A w/ prob p -> train child network of A and gets acc R -> compute gradient of p and scale by R to update RNN -> begin)
- neuroevolution (uses evolutionary algs to gen architectures, its like a natural selection with mutations and evolutions of the network)
- differentiable architecture search (DARTS) (uses continuous relaxation, to let the search space differentiable, allowing gradient descent)
- one-shot NAS (train a large super network, and then tries sub-networks of the large one - **only one training** makes this method fast)
- training-free methods (**super fucking relampo marquinhos fast** - works with a heuristic for the pre-trained arc that correlates with validation acc, so you predict how the arc will do without training)

>more expensive: RNN, neuroevolution and DARTS

>less expensive: one-shot NAS, training-free methods

### reproducibility problem

- there is a research with 800 gpus running by 28 days for classify CIFAR-10 to deal with a complete NAS proccess
- this is too expensive, so we cant reproduce it

### benchmarks

- compare algorhtims against a common baseline
- make NAS more accessible for researchers with fewer pc resources
- can give insight into the NAS search space
- popular benchmarks
    - NAS-Bench-101
    - NAS-Bench-201
    - NAS-Bench-301
    - NATS-Bench


# References

1. Why care about NAS? [https://youtu.be/_dR8a5ZcBgM?si=BZx7c7BzxSQjO9Fs]
