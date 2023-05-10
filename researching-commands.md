# Researching Commands
## Interesting Uses of the `grep` Command ##
`grep` is a command-line tool that lets you find a pattern or expression in a given file, the output returns lines with matches to your string.<br> 

Just as a point of comparison, here is a standard use of grep: <br>
`grep "zebra" zooPamphlet.txt` <br>
_find string "zebra" in a file called "zooPamphlet.txt"_ <br>


We will use the following-line tools for files and directories from `./technical`. <br>
### `grep -e`
Sometimes you want to find a match for more than one expression, in this case you will need to add `-e` before every expression. The command-line input: 

        $ grep -e "bomb" -e "flight" chapter-2.txt
    
Generates the output:
<pre>        
Islam, and celebrated recent suicide <b>bomb</b>ings of American military facilities in the
        Kingdom. It praised the 1983 suicide <b>bomb</b>ing in Beirut that killed 241 U.S. Marines,
        the 1992 <b>bomb</b>ing in Aden, and especially the 1993 firefight in Somalia after which
        November 24, 1989, when a remotely controlled car <b>bomb</b> killed Azzam and both of his
        fatwa demanding their eviction. In December, <b>bomb</b>s exploded at two hotels in Aden
    In November 1995, a car <b>bomb</b> exploded outside a Saudi-U.S. joint facility in Riyadh
    In June 1996, an enormous truck <b>bomb</b> detonated in the Khobar Towers residential
        cloudy are the 1993 <b>bomb</b>ing of the World Trade Center, a plot that same year to
        particular interest in learning how to use truck <b>bomb</b>s such as the one that had
        Dozens of additional militants arrived on later <b>flight</b>s.
        embassy in Nairobi was an easy target because a car <b>bomb</b> could be parked close by,
        Members of the cells rented residences, and purchased <b>bomb</b>-making materials and
        <b>bomb</b>s, and acquired the delivery vehicles. On August 4, they made one last casing
    On the morning of August 7, the <b>bomb</b>-laden trucks drove into the embassies roughly
        permissible under Islam." Asked if he had indeed masterminded these <b>bomb</b>ings, Bin
 </pre>       
Similarly, the command-line input:

        $ grep -e "killed" -e "flight" chapter-2.txt
        
Generates the output:
<pre>
Kingdom. It praised the 1983 suicide bombing in Beirut that <b>killed</b> 241 U.S. Marines,
        especially clear in Egypt. Confronted with a violent Islamist movement that <b>killed</b>
        appeared to be ungainly but was in fact quite athletic, s<b>killed</b> as a horseman,
        November 24, 1989, when a remotely controlled car bomb <b>killed</b> Azzam and both of his
        were <b>killed</b>. The Saudi government arrested four perpetrators, who admitted being
        Americans were <b>killed</b>, and 372 were wounded. The operation was carried out
        <b>killed</b> 241 U.S. Marines in Lebanon in 1983. The relationship between al Qaeda and
        Dozens of additional militants arrived on later <b>flight</b>s.
    The attack on the U.S. embassy in Nairobi destroyed the embassy and <b>killed</b> 12
        attack on the U.S. embassy in Dar es Salaam <b>killed</b> 11 more people, none of them
</pre>        
### `grep -o`
Maybe you want to only output the matched expression without the rest of the line. In this case, you will need to add `-o` after `grep` before expression arguments. The command-line input:

        $ grep -o "killed" chapter-1.txt
        
Generates the output:
<pre>
<b>killed</b>
<b>killed</b>
<b>killed</b>
<b>killed</b>
<b>killed</b>
<b>killed</b>
<b>killed</b>
<b>killed</b>
</pre>
Similarly, the command-line input:

        $ grep -o -e "killed" -e "bomb" chapter-2.txt

Generates the output:
<pre>
<b>bomb</b>
<b>bomb</b>
<b>killed</b>
<b>bomb</b>
<b>killed</b>
<b>killed</b>
<b>bomb</b>
<b>killed</b>
<b>bomb</b>
<b>bomb</b>
<b>killed</b>
<b>bomb</b>
<b>killed</b>
<b>bomb</b>
<b>bomb</b>
<b>killed</b>
<b>bomb</b>
<b>bomb</b>
<b>bomb</b>
<b>bomb</b>
<b>killed</b>
<b>killed</b>
<b>bomb</b>
</pre>

### `grep -n`
Or, perhaps, you want to not only find matches but line numbers for those matches as well. In this case, you will need to add `-n` after `grep` but before expression arguments. The command-line input: 

        $ grep -n "killed" chapter-1.txt

Generates the output:
<pre>
        96:    All on board, along with an unknown number of people in the tower, were <b>killed</b> instantly.
        104:    The hijackers attacked sometime between 8:42 and 8:46. They used knives (as reported by two passengers and a flight attendant), Mace (reported by one passenger), and the threat of a bomb (reported by the same passenger). They stabbed members of the flight crew (reported by a flight attendant and one passenger). Both pilots had been <b>killed</b> (reported by one flight attendant). The eyewitness accounts came from calls made from the rear of the plane, from passengers originally seated further forward in the cabin, a sign that passengers and perhaps crew had been moved to the back of the aircraft. Given similarities to American 11 in hijacker seating and in eyewitness reports of tactics and weapons, as well as the contact between the presumed team leaders, Atta and Shehhi, we believe the tactics were similar on both flights.
        108:    At 8:52, in Easton, Connecticut, a man named Lee Hanson received a phone call from his son Peter, a passenger on United 175. His son told him: "I think they've taken over the cockpit-An attendant has been stabbed- and someone else up front may have been <b>killed</b>. The plane is making strange moves. Call United Airlines-Tell them it's Flight 175, Boston to LA." Lee Hanson then called the Easton Police Department and relayed what he had heard.
        110:    Also at 8:52, a male flight attendant called a United office in San Francisco, reaching Marc Policastro. The flight attendant reported that the flight had been hijacked, both pilots had been <b>killed</b>, a flight attendant had been stabbed, and the hijackers were probably flying the plane. The call lasted about two minutes, after which Policastro and a colleague tried unsuccessfully to contact the flight.
        122:    All on board, along with an unknown number of people in the tower, were <b>killed</b> instantly.
        146:    All on board, as well as many civilian and military personnel in the building, were <b>killed</b>.
        178:    The cockpit voice recorder data indicate that a woman, most likely a flight attendant, was being held captive in the cockpit. She struggled with one of the hijackers who <b>killed</b> or otherwise silenced her.
        190:    Callers reported that a passenger had been stabbed and that two people were lying on the floor of the cabin, injured or dead-possibly the captain and first officer. One caller reported that a flight attendant had been <b>killed</b>.
</pre>
Similarly, the command-line input: 

        $ grep -n -e "killed" -e "bomb" chapter-1.txt

Generates the output:

                72:    The hijackers quickly gained control and sprayed Mace, pepper spray, or some other irritant in the first-class cabin, in order to force the passengers and flight attendants toward the rear of the plane. They claimed they had a bomb.
        84:    Sweeney calmly reported on her line that the plane had been hijacked; a man in first class had his throat slashed; two flight attendants had been stabbed-one was seriously hurt and was on oxygen while the other's wounds seemed minor; a doctor had been requested; the flight attendants were unable to contact the cockpit; and there was a bomb in the cockpit. Sweeney told Woodward that she and Ong were trying to relay as much information as they could to people on the ground.
        96:    All on board, along with an unknown number of people in the tower, were killed instantly.
        104:    The hijackers attacked sometime between 8:42 and 8:46. They used knives (as reported by two passengers and a flight attendant), Mace (reported by one passenger), and the threat of a bomb (reported by the same passenger). They stabbed members of the flight crew (reported by a flight attendant and one passenger). Both pilots had been killed (reported by one flight attendant). The eyewitness accounts came from calls made from the rear of the plane, from passengers originally seated further forward in the cabin, a sign that passengers and perhaps crew had been moved to the back of the aircraft. Given similarities to American 11 in hijacker seating and in eyewitness reports of tactics and weapons, as well as the contact between the presumed team leaders, Atta and Shehhi, we believe the tactics were similar on both flights.
        108:    At 8:52, in Easton, Connecticut, a man named Lee Hanson received a phone call from his son Peter, a passenger on United 175. His son told him: "I think they've taken over the cockpit-An attendant has been stabbed- and someone else up front may have been killed. The plane is making strange moves. Call United Airlines-Tell them it's Flight 175, Boston to LA." Lee Hanson then called the Easton Police Department and relayed what he had heard.
        110:    Also at 8:52, a male flight attendant called a United office in San Francisco, reaching Marc Policastro. The flight attendant reported that the flight had been hijacked, both pilots had been killed, a flight attendant had been stabbed, and the hijackers were probably flying the plane. The call lasted about two minutes, after which Policastro and a colleague tried unsuccessfully to contact the flight.
        116:    At 9:00, Lee Hanson received a second call from his son Peter: It's getting bad, Dad-A stewardess was stabbed-They seem to have knives and Mace-They said they have a bomb-It's getting very bad on the plane-Passengers are throwing up and getting sick-The plane is making jerky movements-I don't think the pilot is flying the plane-I think we are going down-I think they intend to go to Chicago or someplace and fly into a building-Don't worry, Dad- If it happens, it'll be very fast-My God, my God.
        122:    All on board, along with an unknown number of people in the tower, were killed instantly.
        126:    American 77 pushed back from its gate at 8:09 and took off at 8:20. At 8:46, the flight reached its assigned cruising altitude of 35,000 feet. Cabin service would have begun. At 8:51, American 77 transmitted its last routine radio communication. The hijacking began between 8:51 and 8:54. As on American 11 and United 175, the hijackers used knives (reported by one passenger) and moved all the passengers (and possibly crew) to the rear of the aircraft (reported by one flight attendant and one passenger). Unlike the earlier flights, the Flight 77 hijackers were reported by a passenger to have box cutters. Finally, a passenger reported that an announcement had been made by the "pilot" that the plane had been hijacked. Neither of the firsthand accounts mentioned any stabbings or the threat or use of either a bomb or Mace, though both witnesses began the flight in the first-class cabin.
        146:    All on board, as well as many civilian and military personnel in the building, were killed.
        176:    At 9:32, a hijacker, probably Jarrah, made or attempted to make the following announcement to the passengers of Flight 93:"Ladies and Gentlemen: Here the captain, please sit down keep remaining sitting. We have a bomb on board. So, sit." The flight data recorder (also recovered) indicates that Jarrah then instructed the plane's autopilot to turn the aircraft around and head east.
        178:    The cockpit voice recorder data indicate that a woman, most likely a flight attendant, was being held captive in the cockpit. She struggled with one of the hijackers who killed or otherwise silenced her.
        182:    At 9:39, the FAA's Cleveland Air Route Traffic Control Center overheard a second announcement indicating that there was a bomb on board, that the plane was returning to the airport, and that they should remain seated.
        188:    At least ten passengers and two crew members shared vital information with family, friends, colleagues, or others on the ground. All understood the plane had been hijacked. They said the hijackers wielded knives and claimed to have a bomb. The hijackers were wearing red bandanas, and they forced the passengers to the back of the aircraft.
        190:    Callers reported that a passenger had been stabbed and that two people were lying on the floor of the cabin, injured or dead-possibly the captain and first officer. One caller reported that a flight attendant had been killed.
        194:    Passengers on three flights reported the hijackers' claim of having a bomb. The FBI told us they found no trace of explosives at the crash sites. One of the passengers who mentioned a bomb expressed his belief that it was not real. Lacking any evidence that the hijackers attempted to smuggle such illegal items past the security screening checkpoints, we believe the bombs were probably fake.
        230:    The threat of Soviet bombers diminished significantly as the Cold War ended, and the number of NORAD alert sites was reduced from its Cold War high of 26. Some within the Pentagon argued in the 1990s that the alert sites should be eliminated entirely. In an effort to preserve their mission, members of the air defense community advocated the importance of air sovereignty against emerging "asymmetric threats" to the United States: drug smuggling, "non-state and state-sponsored terrorists," and the proliferation of weapons of mass destruction and ballistic missile technology.
        460:    At 9:32, a third radio transmission came over the frequency:"Keep remaining sitting. We have a bomb on board." The controller understood, but chose to respond: "Calling Cleveland Center, you're unreadable. Say again, slowly." He notified his supervisor, who passed the notice up the chain of command. By 9:34, word of the hijacking had reached FAA headquarters.
        462:    FAA headquarters had by this time established an open line of communication with the Command Center at Herndon and instructed it to poll all its centers about suspect aircraft. The Command Center executed the request and, a minute later, Cleveland Center reported that "United 93 may have a bomb on board." At 9:34, the Command Center relayed the information concerning United 93 to FAA headquarters. At approximately 9:36, Cleveland advised the Command Center that it was still tracking United 93 and specifically inquired whether someone had requested the military to launch fighter aircraft to intercept the aircraft. Cleveland even told the Command Center it was prepared to contact a nearby military base to make the request. The Command Center told Cleveland that FAA personnel well above them in the chain of command had to make the decision to seek military assistance and were working on the issue.
        468:    Then, at 9:39, a fourth radio transmission was heard from United 93: Ziad Jarrah: Uh, this is the captain. Would like you all to remain seated. There is a bomb on board and are going back to the airport, and to have our demands [unintelligible]. Please remain quiet.
        470:    The controller responded: "United 93, understand you have a bomb on board. Go ahead." The flight did not respond.
        510:    The news of a reported bomb on board United 93 spread quickly at NEADS. The air defenders searched for United 93's primary radar return and tried to locate other fighters to scramble. NEADS called Washington Center to report: NEADS: I also want to give you a heads-up, Washington.

### `grep -m`
Another interesting take would be to only show a maximum _n_ (where _n_ is a number) times there are matches to the expression. The command-line output:

        $ grep -m 5 "bomb" chapter-2.txt

Generates the output: 
<pre>
        Islam, and celebrated recent suicide <b>bomb</b>ings of American military facilities in the
        Kingdom. It praised the 1983 suicide <b>bomb</b>ing in Beirut that killed 241 U.S. Marines,
        the 1992 <b>bomb</b>ing in Aden, and especially the 1993 firefight in Somalia after which
        November 24, 1989, when a remotely controlled car <b>bomb</b> killed Azzam and both of his
        fatwa demanding their eviction. In December, <b>bomb</b>s exploded at two hotels in Aden
</pre>
Similarly, the command-line input:

        $ grep -m 10 "bomb" chapter-2.txt

Generates the output:
<pre>
        Islam, and celebrated recent suicide <b>bomb</b>ings of American military facilities in the
        Kingdom. It praised the 1983 suicide <b>bomb</b>ing in Beirut that killed 241 U.S. Marines,
        the 1992 <b>bomb</b>ing in Aden, and especially the 1993 firefight in Somalia after which
        November 24, 1989, when a remotely controlled car <b>bomb</b> killed Azzam and both of his
        fatwa demanding their eviction. In December, <b>bomb</b>s exploded at two hotels in Aden
    In November 1995, a car <b>bomb</b> exploded outside a Saudi-U.S. joint facility in Riyadh
    In June 1996, an enormous truck <b>bomb</b> detonated in the Khobar Towers residential
        cloudy are the 1993 <b>bomb</b>ing of the World Trade Center, a plot that same year to
        particular interest in learning how to use truck <b>bomb</b>s such as the one that had
        embassy in Nairobi was an easy target because a car <b>bomb</b> could be parked close by,
</pre>
#### Sources that Helped Inform this Blog:

[Code Snippets for grep Commands](https://www.makeuseof.com/grep-command-practical-examples/) <br>

[grep manual](https://ss64.com/bash/grep.html)

