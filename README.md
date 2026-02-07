# Meta-learning-for-predicting-channel-state-information-in-satellite-communication-systems
This project is exploring the use of ML methods to predict channel quality in satellite communcation systems. First looking at a hybrid Transformer-LSTM implementation and now looking at how meta-learning can be used. 

Transfer knowledge from data-rich geometries (e.g low-band frequencies like 2 GHz, mid-elevation) to data-poor scenarios (e.g higher frequency bands like 12GHz, low elevation) using T-LSTM base learner and residual meta-network, addressing channel aging with few-shot adaptation.

For the first part with only a T-LSTM: A simulation of a satellite constellation is generated in MATLAB, creating a channel state information (CSI) dataset which is then used to train a T-LSTM

Now, with the MetaModelNet approach, i have changed the MATLAB code so that the script generates satellite constellation trajectories and produces channel impulse responses organized by geometry type for meta-learning. It simulates multiple orbital configurations with varying frequencies, elevation angles, and propagation conditions, classifying each continuous satellite pass as Head data-rich or Tail data-poor based on average elevation. For Head geometries, it exports full-duration channel records enabling Python-side k-shot subsampling, while Tail geometries are reserved for few-shot deployment testing.

Currently developing the MetaModelNet code so stay tuned for that to be added here. 