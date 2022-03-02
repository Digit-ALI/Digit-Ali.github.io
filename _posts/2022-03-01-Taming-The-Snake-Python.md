This is to just document an issue I had monday night when trying access the Lab 5 through the website and I wanted to share this processs as it might be helpful to someone else.
I tried to visit lindsaythomas.net to access the Jupyter notebook, but the website gave me an error. 
 
I remembered that we had learned about Github and Jekyll in Lab 1, so out of curiosity I took a look at Professor Thomas' Github account and I found a repository https://github.com/lcthomas/eng612s22-lab5/blob/main/lab5.ipynb -- it was the Jupyter notebook!

I couldn’t run this on the web, however. I had to download the file and figure out how to run it on my own computer. Visual Studio Code offered to open the file, and I saw the contents! I tried to run it, but I got errors. I had to install the correct version of Python – “3.8.9 64-bit” – to my mac. It took a long time, but then I was able to successfully run the first Python cell.

4. Replaced comment with string “another¬¬_example_file.txt”

My questions:
Q: The notebook tells us that we can reference a variable in any cell after it has been defined. What about functions? We define the function split_into_words multiple times; does that create multiple functions? How do we reference each one?

Q: What happens if we indent the first line of a function, the one with the “def” keyword?

Lab 5

Question 1:Once I ran the cell the apostrophe s was left out. The code incorrectly splits out from the contraction of “let’s”, which should be recognized as one word. 
-- ['okay', 'okay', 'ladies', 'now', 'let', 's', 'get', 'in', 'formations']

(note) +
Causes the resulting RE to match 1 or more repetitions of the preceding RE. ab+ will match ‘a’ followed by any non-zero number of ‘b’s; it will not match just ‘a’.

Capital W and Lowercase mean different things. \W Matches any character which is not a word character. This is the opposite of \w. If the ASCII flag is used this becomes the equivalent of [^a-zA-Z0-9_]. If the LOCALE flag is used, matches characters which are neither alphanumeric in the current locale nor the underscore. (,!’.”) Non -alphabetic characters.

If you add + (\W+) the plus in a re indicates to match one or more repeating occurrences of whatever comes before the +. 
Because \W means any character that is not part of the alphabet are re will split whenever it sees one or more non-letter characters.

Question 2: If I run the cell right away without deleting the comment # (because python doesn’t see comments, which are mainly there for humans not computers”. After replacing the text it ran perfectly. 

Question 3: The output of the script is human friendly and displays a neat table. In the table were filenames, the records, authors, date and the number of times vir-ver appeared in those specific texts. What is interesting is that 10 documents were processed but only 9 came back with results. So, one document had neither ver-vir in it. The code said to exclude those that don’t have any results, however running the cell will let you know what was counted. 

Question 4: First, the re is searching for any date that begins with 20. The second line substitutes the empty string for “20” in the date.

I played around to see what would happen if the date was 2006 and I got ‘06’. Then I wondered what would happen if the date was 2020 and I only got “ “. Why is this? Is this the expected behavior?
import re
date = "2006"
if re.search(r'^20', date):
    date = re.sub('20', '', date)
date
'06'

(Caret.) Matches the start of the string, and in multiline mode also matches immediately after each newline.

If you don't know what the regular expression ^20 means in Python regex syntax, how can you find out? One could google this or search the re package documentation.

As I worked this week’s lesson I thought about Prescott and Hughes article “Why do we digitize?” As I begin to work with data sets, code, and other components of computing, I thought why is it important that the transatlantic slave trade is digitized, or why texts (ebooks) add value to our research—why is the old way (simple) not enough? While the easy answers are, remote access, accessibility, and quantification, which are great reasons, what is the larger perspective? This reading resonated with my research on black colonization to Liberia in the 19th century by asking “so what?” What does accessibility, preservation and remote access really do for us or for my project? Prescott and Hughes stated that “the failure or success of projects that employ digital methods to study manuscripts doesn’t hinge on whether not technology preforms, but rather what it allows us to find out—technology is not a deus ex machina.” What we do in the digital humanities is not the end all be all but simply a new beginning for how we understand our research or questions. If you take large scale data and perform a data analysis, patterns can emerge and provide important new questions. One of my goals is to create a map that shows the patterns of migration in colonization, and I am anxious to see what new questions or ideas will come from my data visualization. 
