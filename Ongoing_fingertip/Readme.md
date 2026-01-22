# Fingertip-to-Cortex Spiking Neural Network

This folder contains the implementation of a fingertip-to-cortex spiking neural network (SNN) driven by recorded human skin displacement signals. The model provides an end-to-end, event-based representation of tactile information flow, from mechanoreceptors in the skin to cortical populations, and is designed for reproducible benchmarking of neuromorphic tactile processing.

The pipeline uses experimentally recorded fingertip surface motion as input and converts continuous displacement into sparse spike trains using populations of mechanoreceptors with distinct adaptation dynamics. Neural activity is then propagated through anatomically grounded stages of the ascending somatosensory pathway, including the trigeminal ganglion, brainstem, thalamus, and primary somatosensory cortex.

Skin displacement signals are acquired using laser Doppler vibrometry during ultrasonic stimulation and are preprocessed to match the temporal resolution of the network. Preprocessing includes offset correction, temporal smoothing to approximate viscoelastic skin dynamics, rectification, and normalization. The resulting signal is used to drive mechanoreceptor populations modeled as adaptive exponential integrate-and-fire neurons with spatial receptive fields distributed across the fingertip surface.

The central pathway is implemented as a feed-forward, spike-driven network with sparse connectivity and deterministic dynamics, enabling precise analysis of representational transformations across layers. Activity is analyzed at both the single-neuron and population levels using information-theoretic measures, redundancy metrics, and stimulus decoding. These analyses quantify how tactile information is compressed, decorrelated, and redistributed as signals ascend toward the cortex.

This implementation is intended as a reusable reference for neuromorphic tactile processing, suitable for benchmarking architectures under constraints of latency, sparsity, and energy efficiency. The modular structure allows substitution of neuron models, connectivity patterns, or analysis methods without altering the overall pipeline.
