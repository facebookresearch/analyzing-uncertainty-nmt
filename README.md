# Introduction

This repository contains additional reference translations for the WMT'14 En-De and En-Fr test sets (_newstest2014_) as described in the paper:
[Analyzing Uncertainty in Neural Machine Translation](https://arxiv.org/abs/1803.00047).

In particular we provide 10,000 additional reference translations written by professional translators:
- 10 additional reference translations for each of 500 sentences of the WMT'14 En-De test set (5,000 total)
- 10 additional reference translations for each of 500 sentences of the WMT'14 En-Fr test set (5,000 total)

# Format

Each line in the data file contains a sentence and an identifier, where identifiers represent:
- `S-123` English source for sentence #123 of _newstest2014_
- `T-123`: Original reference translation (German or French)
- `R1-123` through `R10-123`: Additional reference translations

Sentence numbers correspond to the index of the sentence in the full test set (see below).

### Full test sets

The full test sets from which the sentences were sampled can be reconstructed with [sacrebleu](https://github.com/awslabs/sockeye/tree/master/contrib/sacrebleu):
```
sacrebleu --test-set wmt14 --language-pair en-de --echo src
sacrebleu --test-set wmt14 --language-pair en-de --echo ref
sacrebleu --test-set wmt14/full --language-pair en-fr --echo src
sacrebleu --test-set wmt14/full --language-pair en-fr --echo ref
```

# Citation

If you use the data in your paper, then please cite it as:

```
@inproceedings{ott2018analyzing,
  author    = {Ott, Myle and Auli, Michael and Grangier, David and Ranzato, Marc'Aurelio},
  title     = {Analyzing Uncertainty in Neural Machine Translation},
  booktitle = {International Conference on Machine Learning},
  year      = 2018,
}
```

# License
The dataset is licenced under CC-by-NC, see the LICENSE file for details.
