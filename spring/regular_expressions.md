**Regular Expressions in Java**

Regular Expressions (Regex) in Java are a sequence of characters used to define a search pattern for text processing tasks. They help in efficiently matching, searching, and manipulating strings based on specific rules.

* Used for validating input formats like email, phone numbers, and passwords
* Helps in searching and extracting specific patterns from large text data
* Supports powerful text manipulation operations such as find and replace

In Java, regular expressions are supported through the java.util.regex package, which mainly consists of the following classes:

* Pattern: Defines the regular expression.
* Matcher: Used to perform operations such as matching, searching and replacing.
* PatternSyntaxException: Indicates a syntax error in the regular expression.

**Pattern Class**
The Pattern class compiles regex strings into pattern objects.

compile(String regex): Compiles a regex.
matcher(CharSequence input): Creates a matcher to search a string.
matches(String regex, CharSequence input): Checks full-string match.
split(CharSequence input): Splits input based on the pattern.

**Matcher Class**
The Matcher class performs matching operations for input strings.

find(): Searches for pattern occurrences.
start() / end(): Returns start and end indices of a match.
group() / groupCount(): Retrieves matched subsequences.
matches(): Checks if the entire input matches the pattern.

**Important Notes**
1. Use Pattern.compile() to create a regex pattern.
2. Use matcher() on a Pattern to perform matches.
3. Pattern.matches() validates the whole string, while Matcher.find() searches for multiple occurrences.
4. Regex can split text, validate input, and extract data efficiently in Java.

