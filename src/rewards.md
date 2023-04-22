# How Rewards Work

#### _It should be stated that this is an LLMs interpretation and has yet to been altered much, if at all, by a human. I'll remove this note later, I'll double check all files before I push the final version of them._ 

This code defines a `RewardModel` class that inherits from `torch.nn.Module`. The `RewardModel` is used to calculate rewards for completions generated by a language model.

1. `__init__` method initializes the class with `model_path`, `device`, and `config` as arguments. It loads the pre-trained GPT model and tokenizer from the given model path. It also initializes the linear head `v_head` and sets the padding token.

2. `reward` method computes rewards for a list of completions. It takes a list of completions and returns a tensor of rewards for each completion.

3. `forward` method computes the forward pass of the model. It takes input tensors such as `input_ids`, `attention_mask`, etc., and returns a dictionary containing the loss, chosen end scores, and rejected end scores.