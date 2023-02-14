# Week 5 Lab Report

## Exploring the Grep command

### -r

[Source](https://linuxhint.com/use-grep-recursively/)

The -r option performs a recursive search within a directory that may contain other directories. This allows you to condense
your grep command into one line when searching a large database of files.

Input `grep -r "Lucayans" written_2/`

Output `written_2/travel_guides/berlitz2/Bahamas-History.txt: We know them today as the Lucayans. Columbus claimed the island and`

Input `grep -r "1460" written_2/`

Output 
```
written_2/travel_guides/berlitz1/HistoryEdinburgh.txt:        by James III (1460–1488) to be “the principal burgh of our kingdom.”
written_2/travel_guides/berlitz1/IntroEdinburgh.txt:        the reign of James III (1460­–1488), and in the following years it
written_2/travel_guides/berlitz1/WhereToEdinburgh.txt:        reign of Scotland’s James III (1460–1488). The scepter and sword were
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:        is believed to have burned down in 1460.
written_2/travel_guides/berlitz2/Algarve-History.txt:In 1415, long after the Reconquista was completed, a Portuguese fleet assembled on the River Tagus in Lisbon for an assault on the Moors in their homeland. Crossing the Straits of Gibraltar, the armada attacked and seized the North African city of Ceuta. An illustrious member of the famous raid was the young Prince Henry, half Portuguese and half English, the son of King João I and his wife, Philippa of Lancaster. Ceuta would be Henry’s one and only military victory, though he was destined to establish Portugal as a major world power, helping to develop important world trade routes by the time of his death in 1460.
written_2/travel_guides/berlitz2/Portugal-History.txt:Henry died in 1460, but Portugal’s discovery voyages continued. The king who ruled over the golden age of exploration — and exploitation — was Manuel I “The Fortunate,” who reigned from 1495–1521. The many important discoveries that were made during his reign would assure his position as Europe’s richest ruler: He could well afford to erect monuments as elegant as the Tower of Belém and as impressive as the Jerónimos Monastery in Lisbon.
```

### -c

[Source](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) 

The -c option returns a count of the lines that match the given string to search.

Input `grep -c "world" *.txt`

Output 
```
ch1.txt:5
ch10.txt:9
ch3.txt:10
ch4.txt:3
ch5.txt:13
ch6.txt:4
ch7.txt:1
ch8.txt:5
ch9.txt:16
```

Input `grep -c "there" *.txt`

Output
```
ch1.txt:24
ch10.txt:35
ch3.txt:27
ch4.txt:23
ch5.txt:5
ch6.txt:24
ch7.txt:18
ch8.txt:37
ch9.txt:36
```

### -l

[Source](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) 

The -l option additionally prints out a list of the files that contain the matched strings.

Input `grep -r -l "Lucayans" written_2/`

Output
```
written_2/travel_guides/berlitz2/Bahamas-History.txt
```

Input `grep -r -l "weird" written_2/`

Output
```
written_2/non-fiction/OUP/Kauffman/ch6.txt
written_2/travel_guides/berlitz1/WhatToFWI.txt
written_2/travel_guides/berlitz1/WhatToIbiza.txt
written_2/travel_guides/berlitz1/WhereToFrance.txt
written_2/travel_guides/berlitz1/WhereToHongKong.txt
written_2/travel_guides/berlitz1/WhereToIbiza.txt
written_2/travel_guides/berlitz1/WhereToMadrid.txt
written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt
```

### -i

[Source](https://www.geeksforgeeks.org/grep-command-in-unixlinux/) 

The -i option extends the search query to ignore a case-sensitive search string.

Input `grep -r -i " US " berlitz1`

Output
```
berlitz1/HandRJamaica.txt:        Negril; Tel. 957-5200, 957-5204, 800-417-5288 (toll-free from US and
berlitz1/HandRJamaica.txt:        953-9153, 800-330-8272 (toll-free from US and Canada); fax 953-2244;
berlitz1/HandRJamaica.txt:        Tel. 993-2602, 993-2705, 800-633-3284 (toll-free from US or Canada);
berlitz1/HandRJamaica.txt:        Tel. 965-3145, 965-3185, 800-OUTPOST (toll-free from US and Canada);
berlitz1/HandRJamaica.txt:        Andrew’s; Tel. 944-8400, 800-OUTPOST (toll-free from US and Canada);
berlitz1/HandRJerusalem.txt:        Hotel rates in Israel are always quoted in US dollars. The
berlitz1/HandRLosAngeles.txt:        queen-sized beds. Breakfast is not usually included at US hotels,
berlitz1/HistoryEdinburgh.txt:        of the MacAlpin kings. A few shadowy details have been left to us by
berlitz1/HistoryEgypt.txt:        their activities on papyrus paper, helping us to piece together the
berlitz1/HistoryHawaii.txt:        high time for a US coup, and they were able to persuade the US naval
```

Input `grep -r -i "legend" berlitz1`

Output
```
berlitz1/HandRHawaii.txt:        <www.hotelhanamaui.com>. At the end of the legendary road to Hana
berlitz1/HandRIsrael.txt:        Legendary hummous, with very little else on the menu. Very basic, with
berlitz1/HistoryDublin.txt:        myths and legends, later romanticized by Irish writers, that still
berlitz1/HistoryDublin.txt:        persuasion. Many legends surround his mission. It was St. Patrick who
berlitz1/HistoryDublin.txt:        horrendous execution have become the stuff of legend. Daniel O’Connell
berlitz1/HistoryEdinburgh.txt:        “Young Pretender,” which became the stuff of legend.
```
