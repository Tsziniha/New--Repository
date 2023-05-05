# New--Repository
fun binary_search(arr: IntArray, item: Int): Int? {
    var low = 0
    var high = arr.size - 1
    var mid: Int
    var guess: Int?
    
    while (low <= high) {
        mid = (low + high) / 2
        guess = arr[mid]
        
        when {
            guess == item -> return mid
            guess > item -> high = mid - 1
            else -> low = mid + 1
        }
    }
    
    return null
}

fun main() {
    val my_list = IntArray(100000) { it + 1 }
    val item = 12034
    val index = binary_search(my_list, item)
    
    if (index != null) {
        println("The element $item is in $index position")
    } else {
        println("Element $item is not found")
    }
}
#Код бинарного поиска на языке Kotlin
