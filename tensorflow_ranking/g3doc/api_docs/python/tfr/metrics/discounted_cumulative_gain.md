<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tfr.metrics.discounted_cumulative_gain" />
<meta itemprop="path" content="Stable" />
</div>

# tfr.metrics.discounted_cumulative_gain

<!-- Insert buttons and diff -->

<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/ranking/tree/master/tensorflow_ranking/python/metrics.py">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>

Computes discounted cumulative gain (DCG).

```python
tfr.metrics.discounted_cumulative_gain(
    labels, predictions, weights=None, topn=None, name=None,
    gain_fn=_DEFAULT_GAIN_FN, rank_discount_fn=_DEFAULT_RANK_DISCOUNT_FN
)
```

<!-- Placeholder for "Used in" -->

#### Args:

*   <b>`labels`</b>: A `Tensor` of the same shape as `predictions`.
*   <b>`predictions`</b>: A `Tensor` with shape [batch_size, list_size]. Each
    value is the ranking score of the corresponding example.
*   <b>`weights`</b>: A `Tensor` of the same shape of predictions or
    [batch_size, 1]. The former case is per-example and the latter case is
    per-list.
*   <b>`topn`</b>: A cutoff for how many examples to consider for this metric.
*   <b>`name`</b>: A string used as the name for this metric.
*   <b>`gain_fn`</b>: (function) Transforms labels.
*   <b>`rank_discount_fn`</b>: (function) The rank discount function.

#### Returns:

A metric for the weighted discounted cumulative gain of the batch.
