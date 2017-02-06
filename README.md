# number-to-words version 1.0
A C# implementation that accepts a fractional number in string format and returns an object containing the English word translation of the whole part up to Hundreds of Trillion, and the fractional part rounded to two (2) decimal place.


## How it works:

### 1. Calling the method with parameter 'NumberInWords("9101003512035")' will return an object:
```code
{
  whole: "Nine Trillion One Hundred and One Billion Three Million Five Hundred and Twelve Thousand and Thirty Five",
  fraction: "Zero"
}
```

### 2. Calling the method with parameter 'NumberInWords("535.156")' will return an object:
```code
{
  whole: "Five Hundred and Thirty Five",
  fraction: "Sixteen"
}
```

## Usage
1. Download the file "info.dwleke.numbertowords.dll" to your computer
2. Add Reference to the dll in your .NET application
3. Bring the namespace "info.dwleke.numbertowords" to scope in your Class
4. Instantiate an object of the Class "NumberToWord"
5. Call the public function "NumberInWords()" and pass a number in string format.


## Example
A ASP.NET WebAPI implementation of the dll is displayed below:
```code
    [HttpGet]
    public IHttpActionResult GetAmountInWords(string number)
    {
        info.dwleke.numbertowords.NumberToWord numberToWord = new info.dwleke.numbertowords.NumberToWord();
        return Ok(numberToWord.NumberInWords(number));
    }
```


## Usage Scenario
A typical example of where you could use this would be to return an amount in words e.g. $23.12 should read Twenty Three dollar Twelve cent.
To achieve this, all you do is to pass the string "23.12" to the method "NumberInWords()" and you get an object, indicated below, which you could use that data as you desire.
```code
{
  whole: "Twenty Three"
  fraction: "Twelve"
}
```
