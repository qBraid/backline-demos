[<img src="https://qbraid-static.s3.amazonaws.com/logos/Launch_on_qBraid_white.png" width="150">](https://account.qbraid.com?install-project=backline-demos)

# Backline on qBraid

Run [Backline](https://github.com/PennyLaneAI/backline), the open platform from Xanadu and AMD for low-latency quantum-classical programs, in qBraid Lab. Everything runs in your browser. There's nothing to install on your laptop.

Backline lives inside [PennyLane](https://pennylane.ai) and [Catalyst](https://docs.pennylane.ai/projects/catalyst). You write one Python program, and Backline connects the quantum part to the classical engine that does the fast work, such as decoding errors during quantum error correction.

## Start here

1. **Click the button above.** It opens the project page on qBraid. Choose **Launch** and pick an instance. The free 2 vCPU one is enough.
2. **Let Lab set up.** It copies this repository and installs the **PennyLane + Backline** environment, which takes two or three minutes.
3. **Open [`01_steane_ghz_cpu.ipynb`](./01_steane_ghz_cpu.ipynb)** and pick the **PennyLane + Backline** kernel.
4. **Run the cells in order.** The first cell checks your setup.

Only want the files? [Copy the repository into Lab](https://account.qbraid.com?gitHubUrl=https://github.com/qBraid/backline-demos.git) without the environment.

## Notebooks

| Notebook | What it does | Runs on |
|---|---|---|
| [`01_steane_ghz_cpu.ipynb`](./01_steane_ghz_cpu.ipynb) | Encodes a logical GHZ circuit in the Steane code. One CPU role runs the circuit, and a second decodes every error syndrome through Backline. | CPU. About a minute on the free 2 vCPU instance. The optional three-qubit run needs 4 vCPUs. |
| Hierarchical decoding with NVIDIA Ising and PyMatching | Coming next. It needs Catalyst 0.16.0b2, which has no pre-built packages yet. | Planned for CPU and NVIDIA GPU |

## What's in the environment

| Package | Version |
|---|---|
| PennyLane | 0.46.0b1 |
| PennyLane-Lightning | 0.46.0b1 |
| Catalyst | 0.16.0b1 |
| Python | 3.12 |

Backline is a beta and its API may change. These are the September 2026 beta packages. See [`requirements.txt`](./requirements.txt) to build the same setup yourself.

## Not covered here

Xanadu's full demo continues with a remote AMD GPU over RDMA and an AMD Versal VPK120 board. Those steps need that hardware, so they aren't in this repository. Read them in [Xanadu's demo](https://pennylane.ai/demos/backline).

## Learn more

- [How to use PennyLane and Backline](https://pennylane.ai/demos/backline), the demo the first notebook is adapted from
- [Hierarchical QEC decoding with Backline, NVIDIA Ising, and PyMatching](https://pennylane.ai/demos/backline-ising-decoders)
- [Backline whitepaper](https://xanadu.ai/docs/backline-whitepaper.pdf)
- [Backline install guide](https://github.com/PennyLaneAI/backline/blob/main/INSTALL.md)
- [qBraid docs](https://docs.qbraid.com)

## Credits and license

The first notebook is adapted from [How to use PennyLane and Backline for low-latency quantum error correction on GPUs and FPGAs](https://pennylane.ai/demos/backline) by Josh Izaac, Mehrdad Malek, Joseph Lee and Kalman Szenes at Xanadu, from [PennyLaneAI/demos](https://github.com/PennyLaneAI/demos) (Apache 2.0). Changes are listed in [`NOTICE`](./NOTICE). This repository is released under the [Apache 2.0 license](./LICENSE).
