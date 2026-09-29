# Behavioral Capacity Certificates for Quantized Language Models

**Arian Eamaz**  
Department of Electrical and Computer Engineering, University of Illinois Chicago  
aeamaz2@uic.edu

Code, notebooks, frozen protocols, and saved results for Behavioral Capacity
Certificates (BCC). The experiments study behavioral complexity, independent-probe
transfer, forward-only screening, and certified output-head perturbations.

## Complete reproducibility package

Download **BCC_GitHub_Repository.zip** from the [Releases page](https://github.com/eamaz/bcc/releases).
The archive contains all **20 experiment groups**, source code, experiment READMEs,
five notebooks, small-model checkpoints, frozen protocols, and saved evidence.
Extract it and enter the `bcc/` directory. With Python 3.12, run:

```bash
python tools/restore_duplicates.py
python tools/verify_package.py
```

These offline checks restore byte-identical deduplicated files and verify hashes,
Python syntax, notebook payloads, and experiment paths. Open `EXPERIMENT_INDEX.md`
in the extracted package to locate each experiment's instructions. The paper's
public model weights are downloaded using the recorded immutable revisions.

## Colab notebooks

- [OLMoE output-head certificate](OLMoE_Head.ipynb)
- [SmolLM2 output-head certificate](SmolLM2_Head.ipynb)
- [SmolLM2 edit capacity](SmolLM2_Edit_Capacity.ipynb)
- [Qwen2.5 and SmolLM2 cache precision](Modern_Cache.ipynb)
- [Format-only W/A/K/V aggregation](Format_Only.ipynb)

The archive's experiment guides specify environments, hardware requirements,
commands, and saved outputs. Run experiments in a fresh working copy to preserve
recorded evidence. Public large-model weights and omitted regenerable intermediates
are obtained by the supplied scripts.

## License and citation

The original BCC code and accompanying software documentation use the
[MIT License](LICENSE). Third-party code, datasets, and pretrained models retain
their respective licenses and terms. Author metadata is in [CITATION.cff](CITATION.cff).
