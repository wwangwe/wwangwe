
# Me as a Class

```python

from dataclasses import dataclass
from typing import Tuple

class Meta(type):
    def __new__(cls, name, bases, attrs):
        new_cls = super().__new__(cls, name, bases, attrs)
        return dataclass(unsafe_hash=True, frozen=True)(new_cls)

class Bio(metaclass=Meta):
    name        : str = "Timothy Wangwe"
    designation : str = "Data Science"
    base        : str = "Nairobi, Kenya"

class Stack(metaclass=Meta):
    languages   : Tuple[str, ...] = ("Python", "Javascript", "CSS")
    databases   : Tuple[str, ...] = ("SQLite")
    frameworks  : Tuple[str, ...] = ("Django", "Bootstrap4", "Rest API")
    packages    : Tuple[str, ...] = ("Pandas", "Numpy", "Matplotlib", "Seaborn")
    ongoing     : Tuple[str, ...] = ("Sklearn", "Tensorflow", "Keras")

class Social(metaclass=Meta):
    twitter     : str = "Tim_is_Weird"
    linkedin    : str = "Timothy-Wangwe"
```
