# Stimulus Representation in the Ascending Tactile Pathway

This repository contains an end-to-end, event-driven spiking neural network (SNN) model of the ascending tactile pathway, from mechanoreceptors in the periphery to cortical layers, together with analysis tools to quantify information transfer and representational efficiency across stages.
The code accompanies the methods paper “From Skin to Cortex: End-to-End Spiking Neural Network Simulation of Tactile Information Flow” and is designed as a reproducible reference pipeline for neuromorphic tactile processing.

# Overview

The model implements a biologically grounded, feed-forward architecture comprising:

- Mechanoreceptor populations (SA1, SA2, RA)
- Trigeminal ganglion (TG)
- Brainstem (BS)
- Thalamus (VPM)
- Primary somatosensory cortex (layers L4, L3, L2; excitatory and inhibitory populations)

All stages operate in a fully spike-based, event-driven manner, making the pipeline suitable for benchmarking neuromorphic architectures under constraints of latency, sparsity, and energy efficiency.

Two complementary sensory modalities are provided:

- Rodent whisker deflection (biomechanical simulation–driven input)
- Human fingertip skin displacement (recorded vibrometry data)
