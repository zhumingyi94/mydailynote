# Hydra
### MAIN CONTENT
- The main flow for using Hydra: 
	1. Import `hydra` package 
	2. Create configuration folder and .yaml for configuration file 
		![[Pasted image 20240715163003.png | center|775]]
	3. Put decorator in the function we need to execute with `@hydra.main(config_path= ..., config_name)` 
	4. Add the extra parameter in the function `cfg`
		![[Pasted image 20240715170728.png | center|800]]

>[!info]- When configurating some file, for the sake of convenience; we should care about `./` and `../`
> Refer to [[Working with filepath]]

>[!danger]- Hydra changes the working directory to the output directory, so when define path in configuration file, we need to ensure that the files are relative to the current directory

>[!tip]- Hydra integrate really well with integrated class so we can actually use dataclass to define what the structure of configuration object
>Refer to [[Dataclass]]

- Create subconfiguration:
	- Use `defauls`
	![[Pasted image 20240715205310.png | center]]
	- Put `files` in other_config.yaml
	![[Pasted image 20240715205119.png | center]]
	
### QUESTIONS
>[!question]- What is the `config_path` and `config_name`
>`config_path`: Stands for configuration folder
>`config_name`: Stands for name of specific configuration

>[!question]- What `if __name__ == "__main__":` does in Python
>Refer to this note [[Name-Main Idiom]]

>[!question]- What `./` and `../` do in filepath
>Refer to [[Working with filepath]]

>[!question]- How to solve the *danger* case that I mention in the **MAIN CONTENT** section 
>![[Pasted image 20240715183919.png |center]]

##### Syntax-related question
>[!question]- How to add config value
>Use `+` when create a new field 
>For example 
>```bash 
>$ python my_app.py +db.driver=mysql +db.user=omry +db.password=secret
>```


>[!question]- How to override default config values
>Use `++` 
>For example:
>```bash
>$ python my_app.py ++db.password=1234

>[!question]- How to select items from the config group 
>We use `+GROUP=OPTION`
>```bash
>$ python my_app.py +db=postgresql

>[!question]- How to use primary config to override the values from Defaults List
>Using _\_self_\_ after
>![[Pasted image 20240715213024.png]]


>[!question]- How to use the values from Defaults List to override primary config 
>Using _\_self_\_ before
>![[Pasted image 20240715213134.png]]

>[!question]- How to run the same application with multiple different configurations
>Just configure `hydra.mode`
>```bash
>$ python my_app.py hydra.mode=MULTIRUN db=mysql,postgresql schema=warehouse,support,school
>```
>Or, 
>```bash
python my_app.py --multirun db=mysql,postgresql schema=warehouse,support,school
>```
>The quickest way is
>```
python my_app.py -m db=mysql,postgresql schema=warehouse,support,school

>[!question]- How to logging in Hydra 
>```python
>import logging
>from omegaconf import DictConfig
>import hydra
>#A logger for this file
>log = logging.getLogger(__name__)
>@hydra.main()
>def my_app(_cfg: DictConfig) -> None:
>   log.info("Info level message")
>  log.debug("Debug level message")
>  
> if __name__ == "__main__":
>     my_app()
>```

>[!question]- How to print the configuration without running the function 
>Adding `--cfg` or `-c` to the command line like this
>```bash
>$ python my_app.py --cfg job
>```
>`--cfg` have several options:
>1.`job`: Your config 
>2.`hydra`: Hydra config 
>You can also use `--package` or `-p` to display a subset of configuration
>```bash
>$ python my_app.py --cfg hydra --package hydra.job
>```
