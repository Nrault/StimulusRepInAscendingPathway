# Whisker-to-Cortex Spiking Neural Network

This folder contains the implementation of a whisker-to-cortex spiking neural network (SNN) that models tactile information flow in the rodent vibrissal system. The model provides an end-to-end, event-based simulation of the ascending somatosensory pathway, from mechanoreceptors in the whisker follicle to cortical populations, and is designed for reproducible neuromorphic benchmarking.

The pipeline is driven by simulated whisker deflections generated using a biomechanical whisker model. Mechanical forces at the whisker base are extracted and transformed into sparse spike trains by populations of mechanoreceptors with distinct adaptation dynamics. These spike-based representations are then propagated through anatomically grounded stages of the central nervous system, including the trigeminal ganglion, brainstem, thalamus, and layered primary somatosensory cortex.

Whisker stimulation is implemented using ramp-and-hold and vibration paradigms, allowing systematic manipulation of stimulus parameters such as deflection amplitude, direction, velocity, contact location along the whisker, and vibration frequency. These paradigms enable controlled exploration of how different tactile features are encoded and transformed across successive neural stages.

Mechanoreceptors are modeled as adaptive exponential integrate-and-fire neurons tuned to reproduce experimentally observed response profiles of slowly adapting (SA1, SA2) and rapidly adapting (RA) afferents. Central pathway neurons are implemented using biophysically grounded spiking models with sparse, feed-forward connectivity reflecting known anatomical organization. The resulting network operates in a fully spike-driven, deterministic manner, facilitating reproducible analysis and comparison across conditions.

Neural activity is analyzed at each stage of the pathway using information-theoretic measures, redundancy metrics based on pairwise spike-count correlations, and stimulus decoding from both single-neuron and population responses. These analyses quantify how tactile information is redistributed, compressed, and decorrelated as signals ascend from the periphery to the cortex.

This implementation serves as a reference neuromorphic pipeline for tactile processing in the whisker system and is intended for use in benchmarking spike-based architectures, studying representational transformations, and prototyping low-latency sensory processing strategies.
