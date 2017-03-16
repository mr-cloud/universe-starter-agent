**control flow**
1. train.py
    - make the system environments of client-side for remote training.
        - ps, worker, tensorboard and htop four process in one tmux session.
2. **worker.py**
    - make an Universe environment with tensorflow framework and A3C algorithm.
        - **a A3C trainer runs the tf's session within a thread.**
    - worker and ps run on the same cluster for data parallel.
    - share the model and metadata with tensorboard by log.
3. envs.py
    - build an Universe environment with gym.
4. **a3c.py**
    - implementation of A3C algorithm with tensorflow.
5. **model.py**
    - provide the core policy for A3C algorithm.