# Dataclass
**Objective: ** Define new datatype for other to use (maybe configuration objects)

**Main content**

The syntax is like this
```python 
from dataclasses import dataclass 
@dataclass #This helps define the new type for objects
class Paths:
	log: str
	data: str

@dataclass 
class Files:
	train_data: str
	train_labels: str
	test_data: str
	test_labels: str

@dataclass
class Params:
	epoch_count: int 
	lr: float 
	batch_size: int 

@dataclass 
class MNISTConfig:
	paths: Paths
	files: Files
	params: Params
```


>[!question] How to incorporate this in Hydra 
>1. Specify the type `cfg` in `main.py`
>![[Pasted image 20240715190257.png|450]]
>2. We also have to create a `ConfigStore`
> ```python 
> from hydra.core.config_store import ConfigStore # Import this in the begining in order to use ConfigStore
> ...
> cs = ConfigStore.instance()
> cs.store(name="mnist_config", node=MNISTConfig)
>```
> 3. Enjoy