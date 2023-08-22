# Lexacom-Coding-Task
How I came to the final solution.

First String Processing:

The initial text for the first string is provided.

The string "[["new-line"]]" is replaced with the Environment.NewLine to create line breaks where [[new-line]] appeared. This modified string is stored in modifiedFirstString.

Extracting NHS Numbers and Names (First String):
The ExtractNhsNumbers function uses regular expressions to find instances of           "NHS Number:" followed by any non-space characters. These matches are collected in the nhsNumbers list.

The ExtractNames function uses regular expressions to find instances of "Name:" followed by any characters that are not "NHS". These matches are collected in the names list.

Creating Dictionary (First String):
The CreateNameNhsDictionary function takes the lists of extracted names and NHS numbers and creates a dictionary where the names are the keys and the corresponding NHS numbers are the values.
Displaying Edited First String:

The edited first string is displayed with line breaks in place of [[new-line]].

Displaying Table (First String):
The DisplayTable function formats and displays the table of names and NHS numbers for the first string. It prints the header, each name along with its NHS number, and a separator line.

Second String Processing:
The second string in JSON format is provided.

The JSON data is parsed using the JArray.Parse method from the Newtonsoft.Json.Linq namespace.

Extracting NHS Numbers and Names (Second String):
A loop iterates through each object in the JSON array (each representing a person).
For each object, the Name and NHSNumber values are extracted using the .Value<string>("PropertyName") method. Extracted values are stored in the nhsNumbersSecond and namesSecond lists, respectively.

Creating Dictionary (Second String):
Similar to the first string, a dictionary is created for the second string using the namesSecond and nhsNumbersSecond lists.

Displaying Table (Second String):
The DisplayTable function is used again to display the table of names and NHS numbers for the second string.

In summary, this code processes two given strings. For the first string, it replaces [[new-line]] with line breaks, extracts names and NHS numbers, creates a dictionary, and displays both the edited string and the table. For the second string, it parses JSON data, extracts names and NHS numbers, creates a dictionary, and displays the table.
