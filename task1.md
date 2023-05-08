## All instances of Layer Normalization in JoeyNMT

### encoders.py

In `encoders.py` layer normalization is implemented on lines 215/216 and 252/253

```python
215:        self.layer_norm = (nn.LayerNorm(hidden_size, eps=1e-6) if kwargs.get(
216:            "layer_norm", "post") == "pre" else None)


252:        if self.layer_norm is not None:
253:            x = self.layer_norm(x)

```

### decoders.py
```python
534:        self.layer_norm = (nn.LayerNorm(hidden_size, eps=1e-6) if kwargs.get(
535:            "layer_norm", "post") == "pre" else None)

# in the forward() function
588:        if self.layer_norm is not None:
589:            x = self.layer_norm(x)

```

### transformer_layers.py
in transformer_layers.py, 

```python
141        self.layer_norm = nn.LayerNorm(input_size, eps=1e-6)
```