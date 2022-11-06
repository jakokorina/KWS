# KWS

## Homework 2 DLA Kokorina Yulia

Checkpoints are located in models/ folder.

## Experiments
1.  I distilled model by reducing number of channels in conv and reducing hidden size of GRU. It worked, the best model achieved 2e-88 val metric, reduced the model size 4 times and gave a speed-up rate of 3.4.

2. Then I tried to reduce parameter of nn.Linear in Attention, it made a slightly better result but nothing crazy.

3. Then I tried to teach RNN instead of LSTM, it didn't gave necessary val metric.

3. Then I halfed model parameters, which gave me fantastic memory reduction rate(7.27).

4. Then I teached LSTM model using layer distillation, it gave good val metric but made all rates bigger. Then I tried making the same thing with RNN twice, but it didn't work either.

## Streaming model

It works using 

```
git clone https://github.com/jakokorina/KWS.git

python3 stream.py
```

The major challenge was searching for the implementations of all methods because nobody has showed it to us. Another challenge was finding wavs for the plots which you can see at the very end of my ipynb.
