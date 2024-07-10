# 🐍 Python 規範

## 📋目錄

- [命名規則](#命名規則)
- [函數](#函數)
- [註釋](#註釋)

### 命名規則

命名需要代表本身意義, 如 `name` `age` 等等
命名需要在字數和可讀性之間取得平衡，盡量避免使用無意義的變數名稱如 `i` `x` `y`等
可以使用常見的縮寫來代替長名稱，如`df`用來代替`dataframe`

- Class 使用 CamelCase。
- function 和 val 名使用 snake\_case。

### 函數

function 使用 snake_case 來命名, 盡可能地從名字就能得知本身的意思，如 `get_person_by_id` : 利用 id 找出某人
function 需要定義帶入的 parm 和 return, 如 `get_person_by_id(id:str) -> dict` : 定義要有一個字串 id，並且回傳一個 dict
複雜的 function 內部需要 docstrings 來編寫註釋，通常會定義 `功能` , `參數` , `回傳` 或是 `範例`
如 :

```python
def fibonacci(n:int) -> int:
    """
    Return the nth Fibonacci number.
  
    Args:
        n : The position of the Fibonacci number to return.
  
    Returns:
        The nth Fibonacci number.
    """
    if n <= 1:
        return n
    else:
        return fibonacci(n-1) + fibonacci(n-2)
```

### 註釋

- 使用 docstrings 註釋 function 和 Class。
- 代碼中關鍵部分需加註釋。
