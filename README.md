# number-to-words-en

A C# implementation that accepts a fractional number in string format and returns an object containing the English word translation of the whole part up to Hundreds of Trillion, and the fractional part rounded to two (2) decimal place.

##Examples:

1. Calling the method below with parameter NumberInWords("9101003512035") will return an object:
{
  whole: "Nine Trillion One Hundred and One Billion Three Million Five Hundred and Twelve Thousand and Thirty Five",
  fraction: "Zero"
}

2. Calling the method below with parameter NumberInWords("535.156") will return an object:
{
  whole: "Five Hundred and Thirty Five",
  fraction: "Sixteen"
}
