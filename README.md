
## 指定した値を配列の中から近い値のindexを取得するロジックです。

```swift
func findNearIndex(array: [Int], p: Int) -> Int {
    var tmp: Int = 0
    var min: Int = 100
    var found: Int = 0
    for (index, _) in array.enumerated() {
        tmp = array[index] - p
        if abs(min) > abs(tmp) {
            min = tmp
            found = index;
        }
    }
    return found
}
let array = [10, 28, 46, 64]
let currentIndex: Int = 48
findNearIndex(array: array, p: currentIndex)
```
