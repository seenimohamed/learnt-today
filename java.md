# Java related stuffs

## Quick notes about java comparator

#### Possible outcomes :
> -1 : obj1 is bigger than obj2
>  0 : obj1 is equal to obj2
>  1 : obj1 is smaller than obj2

#### Swap rules :
>    -1 : Swap
>  0, 1 : No swap

#### Usage :
    For eg : want to sort with 2 conditions, (i) descending sort based on number (ii) on top of same number do ascending order sort

```
list.sort((String s1, String s2) -> {
    int valueCompare = v2.compareTo(v1);  // number sort in descending order
    int keycompare = k1.compareTo(k2); //string sort in ascending order
    if(valueCompare < 0 || (valueCompare == 0 && keycompare < 1)) {
        return -1;
    }
    return 1;
});
```
