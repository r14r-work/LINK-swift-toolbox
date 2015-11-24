# A Cookbook of Swift String functions

## String Creation

var str = "Hello, playground" // Mutable string
let language = "Swift" // Immutable string

var str1: String
var str2: String = "hello world"

## String Length

let stringLength = str.characters.count

## String Equality

if str == "Hello, playground" {
    print("Strings are Equal")
}

## Case Insensitive Comparison

let nativeLanguage = "French"
if nativeLanguage.caseInsensitiveCompare("french") == .OrderedSame { // NSComparisonResult.OrderedSame
    print("Strings are equal")
}


## String Inequality

if str != "Hello world" {
    print("Strings are NOT Equal")
}

## Test for Empty String
var aString = ""
if aString.isEmpty {
    print("String is empty")
}


## Concatenate

str1 = "Hello, "
str2 = "playground"

str = str1 + str2 // Swift's concatenate operation
str = "\(str1)\(str2)" // Using String interpolation

## Append string

str = "hello"
str += " world"

## Append a single character

let period: Character = "."
str.append(period)

## Prepend string

_ = "My \(str)" // Ignoring result
_ = "My " + str

## Simple CSV split
let csv = "one,two,3"

let anArray = csv.componentsSeparatedByString(",")
print(anArray)

## Join string to CSV
anArray.joinWithSeparator(",")

## String Contains a Substring

str = "www"
let url = "https://www.h4labs.com/"

if url.rangeOfString(str) != nil {
    print("Contains string: \(str)")
}

## String begins with/Has prefix

url.hasPrefix("https:")

## String ends with/Has suffix
url.hasSuffix("/")

## Trim White Space

var blogTitle = "  Swift Cookbook  ".stringByTrimmingCharactersInSet(NSCharacterSet.whitespaceCharacterSet())

// Also remove newlines
blogTitle = "  Swift Cookbook  \n".stringByTrimmingCharactersInSet(NSCharacterSet.whitespaceAndNewlineCharacterSet())

## Uppercase

var company = "apple computer"
company = company.uppercaseString

## Capitalize/Title case

company = company.capitalizedString // capitalize every word
company = company.localizedCapitalizedString // capitalize every word localized


## Lowercase

company = company.lowercaseString

## Loop Over Ever Character of String
for character in "hello world".characters {
    print(character)
}

## String to Int
let aNumberStr = "10"
let anInt: Int? = Int(aNumberStr)

## String to Double
let aDouble: Double? = Double(aNumberStr)

//: