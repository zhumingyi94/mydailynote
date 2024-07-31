# __name__=="Main"

**Overview:** This section explains how `__name__ == "__main__"` works

**Main content:**

Whenever we import a file for example:
```python 
#script1.py
print("This is the first module: {}".format(__name__))
```
```python
#script2.py 
import script1
print("This is the second module: {}".format(__name__)")
```
If we run `script1.py` alone the output will be
```log 
This is the first module: __main__
```
and when we try `script2.py` the output will be
```log 
This is the first module: __script1__
This is the second module: __main__
```
>[!info] When we `import sth` the code in that imported file will be execute immediately 

So how to run only what we need from the imported file ? That's why we have `if __name__ = "__main__"`. When putting any logic code under `if __name__ == "__main__"` statement, the code only execute when you directly run the original script. Look at these examples:

First, we modify `script1.py`:
```python
#script1.py 
def main():
	print("This is the first module: {}".format(__name__))
if __name__ == "__main__":
	main()
```
Given that the `script2.py` not change at all, when we execute `python script1.py` the output remain the same
```log 
This is the first module: __main__
```
but when we execute `python script2.py` now the output become
```log 
This is the second module: __main__
```
Notice that now the `main()` in `script1.py` is not executed in `script2.py` that means the `name-main idiom` like this will greatly help if we want to test independent code logic and not affect the other file that import from the file we're working on

>[!question]- But what if we want to use the function in `if __name__ == "__main__":`
> SIMPLE! Just write the code like this
> ```python 
> # script2.py
> import script1
> script1.main() # use imported_name.name_of_method
> print("This is the second module: {}".format(__name__)")
