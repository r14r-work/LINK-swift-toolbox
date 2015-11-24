# swift-toolbox


## Swift Cookbok: Arrays
var anArray = ["one", "two", "three","one"] // Mutable 
let anImmutableArray = ["four", "five"] // Immutable

## first element of array

anArray.first // a Swift solution. nil if empty 
anArray[0] // Classic solution. Error if empty

## last element of array

anArray.last // a Swift solution. nil if empty 
anArray[anArray.count-1] // Classic solution. Error if empty

## Empty Array

var emptyArray:[String] = [] 
if emptyArray.isEmpty { print("Empty Array") } 
emptyArray.first // Returns nil 
emptyArray.last  // Returns nil

## Does value exist in array?

if anArray.contains("three") { print("Array contains value") }

## How to filter array to get unique items?

// Create a Set then build array from it. Set guarantees uniqueness 
var aSet:Set <string>= [] 
anArray.forEach{aSet.insert($0)} // Could do this: aSet = Set(anArray)
aSet.count 
anArray = Array(aSet) 
anArray.count</string>

## How to merge arrays?

// Just like prior solution. Uses Set's union function // Also skip closure anArray = ["one", "two", "three","one"] 
aSet = Set(anArray) 
aSet.unionInPlace(anImmutableArray) 
aSet.count 
anArray = Array(aSet) 
anArray.count

## Sort Array

anArray = ["one", "two", "three","one"] 
let sortedArray = anArray.sort() // Returns a new sorted array sortedArray anArray 
anArray.sortInPlace() // Update the array in place 
anArray

## Find the index of an element in an Array

anArray = ["one", "two", "three","one"] 
anArray.indexOf("two") // indexOf() can also be used to search an array 
let aNumericArray = [1, 2, 10, 20, 100] 
let x = aNumericArray.indexOf({$0 > 10}) // Find the index of first value greater than 10 x