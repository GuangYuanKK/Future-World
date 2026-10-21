# FutureWorld: A Plug-and-Play Causal Next-State Predictor for Interactive Video World Exploration

**[Project Page](https://GuangYuanKK.github.io/futureworld)**

## Authors

Guangyuan Li<sup>1,2</sup> · Kelu Yao<sup>3,&#42;</sup> · Shuolin Xu<sup>4</sup> · Xinlei Yu<sup>2</sup> · Wei Xing<sup>1</sup> · Lei Zhao<sup>1,&#42;</sup> · Peng-Tao Jiang<sup>5</sup> · Xiaogang Xu<sup>1</sup> · Xiaobin Hu<sup>2,&#42;</sup>

<sup>1</sup>Zhejiang University · <sup>2</sup>National University of Singapore · <sup>3</sup>Zhejiang Lab · <sup>4</sup>Bournemouth University · <sup>5</sup>vivo BlueImage

\*Corresponding authors

## Abstract

Interactive video world models aim to follow user actions while maintaining scene consistency over extended interactions. History-based methods reuse generated latents to preserve scene content, but three limitations of this reuse contribute to error recirculation. (1) The latent generated at each interaction is retained as history, potentially containing blurred details, geometric distortions, or semantic drift. (2) Although retrieved historical content matches the current scene, it can still contain errors that are carried into the next chunk. (3) New outputs then become history for later interactions, potentially reinforcing the same errors through repeated reuse.

To limit this cycle, we predict the future scene state from the current generated latent and the next action before generating the next interaction’s video chunk. This future-state prior guides the next chunk, with the aim of reducing the errors carried forward from history. We propose a plug-and-play Causal Next-Chunk Predictor (C-NCP) with cross-model adaptability and prediction-guided modulation. C-NCP is integrated into four base generators and evaluated across three benchmarks for interactive long-video generation and action-conditioned world modeling. The experiments show reduced error accumulation and improved long-horizon consistency across generation settings.

## Model

<p align="center">
  <img src="assets/model.png" alt="Overview of FutureWorld. The Causal Next-Chunk Predictor maps each frozen generator’s latent into a shared space, forecasts the next chunk, and uses that prediction to modulate autoregressive generation." width="100%">
</p>
