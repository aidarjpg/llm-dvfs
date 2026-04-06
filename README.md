# llm-dvfs

Scripts and training utilities for DVFS-aware NLP experiments on edge GPU platforms, with a focus on BERT-family workloads, tegrastats-based power/performance logging, and controlled frequency experiments.

## Included Content

- Frequency sweep scripts for QNLI, BERT-tiny, BERT-tiny SST-2, and BERT-large
- Baseline and mode-2 experiment runners
- CPU and GPU frequency helper scripts
- Training code for Full Fine-Tuning, BitFit, and LoRA-style runs
- Parsing and visualization utilities for tegrastats logs and event overlays
- Methodology notes in `chapter3_methodology_answers.txt`

## Key Files

### Experiment Scripts

- `run_gpu_freq_experiment_qnli.sh`
- `run_gpu_freq_experiment_bert_tiny.sh`
- `run_gpu_freq_experiment_bert_tiny_sst2.sh`
- `run_gpu_freq_experiment_bert_large.sh`
- `run_mode2_baselines.sh`
- `run_mode2_reruns.sh`
- `run_baseline_experiment.sh`
- `run_experiment.sh`
- `run_experiment_l2.sh`
- `cpu_setfreq.sh`
- `gpu_setfreq.sh`

### Python

- `BERT_sst2_FullFT.py`
- `BERT_BitFit_detailed_timing.py`
- `BERT_BitFit_events_log.py`
- `BERT_FullFT_detailed_timing.py`
- `BERT_FullFT_events_log.py`
- `BERT_LoRA_detailed_timing.py`
- `parse_tegrastats_labeled.py`
- `parse_tegrastats.py`
- `parse.py`
- `overlay_events_tegrastats.py`
- `power_graph.py`
- `monitor_gpu_log.py`
- `run_inference.py`
- `test_memory_qnli.py`

## Basic Workflow

1. Set CPU/GPU frequencies with the helper scripts.
2. Launch one of the experiment runners.
3. Collect `tegrastats` output during training or inference.
4. Parse and label the measurements with the parsing utilities.
5. Visualize or summarize the resulting power/performance behavior.


