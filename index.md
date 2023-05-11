Resource: [grep manual]([https://man7.org/linux/man-pages/man1/grep.1.html])

---
# First Command

## First Command First Example

Command:
```
$ grep -n "Delta" stringsearch-data/technical/911report/chapter-1.txt
```

Output:
```
158:    United 175 was hijacked between 8:42 and 8:46, and awareness of that hijacking began to spread after 8:51. American 77 was hijacked between 8:51 and 8:54. By 9:00, FAA and airline officials began to comprehend that attackers were going after multiple aircraft. American Airlines' nationwide ground stop between 9:05 and 9:10 was followed by a United Airlines ground stop. FAA controllers at Boston Center, which had tracked the first two hijackings, requested at 9:07 that Herndon Command Center "get messages to airborne aircraft to increase security for the cockpit." There is no evidence that Herndon took such action. Boston Center immediately began speculating about other aircraft that might be in danger, leading them to worry about a transcontinental flight-Delta 1989-that in fact was not hijacked. At 9:19, the FAA's New England regional office called Herndon and asked that Cleveland Center advise Delta 1989 to use extra cockpit security.
448:    Right after the Pentagon was hit, NEADS learned of another possible hijacked aircraft. It was an aircraft that in fact had not been hijacked at all. After the second World Trade Center crash, Boston Center managers recognized that both aircraft were transcontinental 767 jetliners that had departed Logan Airport. Remembering the "we have some planes" remark, Boston Center guessed that Delta 1989 might also be hijacked. Boston Center called NEADS at 9:41 and identified Delta 1989, a 767 jet that had left Logan Airport for Las Vegas, as a possible hijack. NEADS warned the FAA's Cleveland Center to watch Delta 1989. The Command Center and FAA headquarters watched it too. During the course of the morning, there were multiple erroneous reports of hijacked aircraft. The report of American 11 heading south was the first; Delta 1989 was the second.
450:    NEADS never lost track of Delta 1989, and even ordered fighter aircraft from Ohio and Michigan to intercept it. The flight never turned off its transponder. NEADS soon learned that the aircraft was not hijacked, and tracked Delta 1989 as it reversed course over Toledo, headed east, and landed in Cleveland.
602:    At 9:44, NORAD briefed the conference on the possible hijacking of Delta 1989. Two minutes later, staff reported that they were still trying to locate Secretary Rumsfeld and Vice Chairman Myers. The Vice Chairman joined the conference shortly before 10:00; the Secretary, shortly before 10:30. The Chairman was out of the country.
604:    At 9:48, a representative from the White House shelter asked if there were any indications of another hijacked aircraft. The deputy director for operations mentioned the Delta flight and concluded that "that would be the fourth possible hijack." At 9:49, the commander of NORAD directed all air sovereignty aircraft to battle stations, fully armed.
[cs15lsp23ga@ieng6-201]:lr3:182$ grep "Delta 1989" stringsearch-data/technical/911report/chapter-1.txt
    United 175 was hijacked between 8:42 and 8:46, and awareness of that hijacking began to spread after 8:51. American 77 was hijacked between 8:51 and 8:54. By 9:00, FAA and airline officials began to comprehend that attackers were going after multiple aircraft. American Airlines' nationwide ground stop between 9:05 and 9:10 was followed by a United Airlines ground stop. FAA controllers at Boston Center, which had tracked the first two hijackings, requested at 9:07 that Herndon Command Center "get messages to airborne aircraft to increase security for the cockpit." There is no evidence that Herndon took such action. Boston Center immediately began speculating about other aircraft that might be in danger, leading them to worry about a transcontinental flight-Delta 1989-that in fact was not hijacked. At 9:19, the FAA's New England regional office called Herndon and asked that Cleveland Center advise Delta 1989 to use extra cockpit security.
    Right after the Pentagon was hit, NEADS learned of another possible hijacked aircraft. It was an aircraft that in fact had not been hijacked at all. After the second World Trade Center crash, Boston Center managers recognized that both aircraft were transcontinental 767 jetliners that had departed Logan Airport. Remembering the "we have some planes" remark, Boston Center guessed that Delta 1989 might also be hijacked. Boston Center called NEADS at 9:41 and identified Delta 1989, a 767 jet that had left Logan Airport for Las Vegas, as a possible hijack. NEADS warned the FAA's Cleveland Center to watch Delta 1989. The Command Center and FAA headquarters watched it too. During the course of the morning, there were multiple erroneous reports of hijacked aircraft. The report of American 11 heading south was the first; Delta 1989 was the second.
    NEADS never lost track of Delta 1989, and even ordered fighter aircraft from Ohio and Michigan to intercept it. The flight never turned off its transponder. NEADS soon learned that the aircraft was not hijacked, and tracked Delta 1989 as it reversed course over Toledo, headed east, and landed in Cleveland.
    At 9:44, NORAD briefed the conference on the possible hijacking of Delta 1989. Two minutes later, staff reported that they were still trying to locate Secretary Rumsfeld and Vice Chairman Myers. The Vice Chairman joined the conference shortly before 10:00; the Secretary, shortly before 10:30. The Chairman was out of the country.
```

Explanation: In the example above I use -n which gives back the line numbers as well as the text in the line numbers that contain the given string.

## First Command Second Example

Command:
```
$ grep -n "final" stringsearch-data/technical/911report/chapter-1.txt
```

Output:
```
20:    It would be their final conversation.
594:    Operators worked feverishly to include the FAA, but they had equipment problems and difficulty finding secure phone numbers. NORAD asked three times before 10:03 to confirm the presence of the FAA in the teleconference. The FAA representative who finally joined the call at 10:17 had no familiarity with or responsibility for hijackings, no access to decisionmakers, and none of the information available to senior FAA officials.
```

Explanation: In the example above I changed the word to final rather than Delta and it displayed fewer lines than before.

---
# Second Command

## Second Command First Example

Command:
```
$ grep -c "Delta" stringsearch-data/technical/911report/chapter-1.txt
```

Output:
```
5
```

Explanation: The option -c is used to count the amount of lines that the string shows up inside. The example shows that within the text file there are 5 lines that contain the word Delta.

## Second Command Second Example

Command:
```
$ grep -c "final" stringsearch-data/technical/911report/chapter-1.txt
```

Output:
```
2
```

Explanation: The example above is using -c to count the amount of lines that final shows up in which is less than the example before it.

---
# Third Command

## Third Command First Example

Command:
```
$ grep -o "Delta" stringsearch-data/technical/911report/chapter-1.txt
```

Output:
```
Delta
Delta
Delta
Delta
Delta
Delta
Delta
Delta
Delta
Delta
```

Explanation: The command -o takes the string given into the command and prints the word for every instance that it is found within the txt file.

## Third Command Second Example

Command:
```
$ grep -o "final" stringsearch-data/technical/911report/chapter-1.txt
```

Output:
```
final
final
```

Explanation: The example is similar to the one above, but uses the word final instead which outputs only two instances where it happens.

---
# Fourth Command

## Fourth Command First Example

Command:
```
$ grep -L "Delta" stringsearch-data/technical/911report/*.txt
```

Output:
```
stringsearch-data/technical/911report/chapter-10.txt
stringsearch-data/technical/911report/chapter-11.txt
stringsearch-data/technical/911report/chapter-12.txt
stringsearch-data/technical/911report/chapter-13.1.txt
stringsearch-data/technical/911report/chapter-13.3.txt
stringsearch-data/technical/911report/chapter-13.4.txt
stringsearch-data/technical/911report/chapter-13.5.txt
stringsearch-data/technical/911report/chapter-2.txt
stringsearch-data/technical/911report/chapter-5.txt
stringsearch-data/technical/911report/chapter-6.txt
stringsearch-data/technical/911report/chapter-7.txt
stringsearch-data/technical/911report/chapter-9.txt
stringsearch-data/technical/911report/preface.txt
```

Explanation: The last option on this lab report for grep is -L which displays all the files that the given string shows up in. In the example it searches the 911report file for all the txt files that contain the word "Delta' within it.

## Fourth Command Second Example

Command:
```
$ grep -L "final" stringsearch-data/technical/911report/*.txt
```

Output:
```
stringsearch-data/technical/911report/chapter-10.txt
stringsearch-data/technical/911report/chapter-11.txt
```

Explanation: In this example the string is "final" and is searched in the 911report file, which only finds two instances where the word shows up.
