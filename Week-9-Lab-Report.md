# **Lab 5**

The command that I will be focusing on today is the **grep** command. 

## Option 1: -v

### Example 1
      grep -v "the" HistoryEdinburgh.txt
        A Brief History
        excavations have revealed evidence of habitation here as long ago as
        Romans and Britons
        The MacAlpin Kings
        close to Perth. His great-great-great-grandson, Malcolm II (1005–1034),
        Malcolm II’s own grandson, Malcolm Canmore (1058–1093),
        often visited Edinburgh with his wife Margaret, a Saxon princess. They
        Queensferry. Margaret was a deeply pious woman who was subsequently
        canonized, and her youngest son, David I (1124–1153), founded a church
        royal burghs (towns with special trading privileges), including
        monks, or “canons,” of Holyrood.
        At this time Edinburgh was still a very modest town, but
        David’s successor, Malcolm IV (1153–1165), made its castle his main
        ended and Canongate began.
        Wars of Independence
        Annandale. The guardians of Scotland were unable to decide who should
        seeing this invitation as a chance to assert his claim as overlord of
        two.
        Edward treated King John as a vassal. However, when Edward
        Edward was furious, and his reprisal was swift and bloody.
        In 1296 he led a force of nearly 30,000 men into Scotland and captured
        was broken up. Oaths of fealty were demanded from Scottish nobles,
        country. Scotland became little more than an English county.
        English garrisons and make raids into English territory. When Wallace
        1292. He was crowned King of Scots at Scone in 1306 and began his
        Edward I died in 1307 and was succeeded by his ineffectual
        son, Edward II, who in 1314 led an army of some 25,000 men to confront
        negotiated at Edinburgh in 1328.
        feared to lose. These divisions — later hardened by religious
        schism — would forever deny Scotland a truly united voice.
        resumed, aggravated by civil war at home as Edward Balliol (son of
        king, Edward III.
        The Stewart Dynasty
        occupied several times by English garrisons. In 1341 it was taken from
        exile in France and made it his principal royal residence, building a
        Battery. He died in 1371 and was succeeded by his nephew, Robert II.
        monarchs who would reign over Scotland — and, subsequently, Great
        Edinburgh emerged as Scotland’s main political center and was declared
        capital of Scotland by constructing a royal palace at Holyrood. He
        Rose — but this did not prevent him from making a raid into England in
        draw closer to England or seek help from her old ally, France. The
        adult James leaned toward France and in 1537 took a French wife, Mary
        at Falkland Palace. On 8 December 1542 a messenger arrived with news
        Mary, Queen of Scots
        reached London, Henry VIII saw his chance to subdue Scotland again and
        Scots refused, and Henry sent an army rampaging through Scotland on a
        But more was at stake than simply Scotland’s independence:
        François II became king of France in 1559 but died soon
        The six years of Mary’s reign were turbulent ones. She
        clashed early on with Edinburgh’s famous Protestant reformer, John
        Knox, who held sway in St. Giles but later adopted an uneasy policy of
        religious tolerance. In 1565 she married her young cousin Henry, Lord
        to a son, Prince James.
        Within a year, however, Darnley was murdered, and Mary
        Mary sought asylum in England, only to be imprisoned by
        Elizabeth. The English queen kept her cousin in captivity for 20 years
        and finally had her beheaded on a trumped-up charge of treason. So it
        was bitterly ironic when Elizabeth died without an heir and James,
        In 1603 James VI of Scotland was thus crowned James I of
        same monarch.
        The Covenanters
        Edinburgh’s population grew fast between 1500 and 1650, and
        in 1625, succeeded by his son, Charles I, who proved an incompetent
        and rioting.
        The next year, a large group of Scottish churchmen and
        Scotland suffered ten years of military rule under Cromwell’s
        Commonwealth.
        Scotland’s troubles continued after Charles II’s
        of Covenanters were imprisoned and executed.
        Presbyterianism was established as Scotland’s official state church and
        Act of Union
        On 1 May 1707 England and Scotland were formally joined
        Scotland was allowed to retain its own legal system, education system,
        James VII), raised an army of Jacobite highlanders and swept through
        he invaded England, capturing Carlisle and driving south as far as
        Derby, only 200 km (130 miles) short of London.
        Highlands before escaping in a French ship. He died in Rome in 1788,
        disillusioned and drunk.
        The Scottish Enlightenment
        The Jacobite uprisings found little support in such lowland
        and previously unknown architect, James Craig, was approved and work
        began.
        This architectural renaissance in Edinburgh was followed by
        David Hume, author of A Treatise of Human Nature and one of Britain’s
        greatest philosophers; Adam Smith, author of The Wealth of Nations, a
        poems and Walter Scott’s novels rekindled interest in Scotland’s
        history and nationhood; Scott especially worked hard to raise
        Scotland’s profile.
        The Modern City
        growth of baking, distilling, printing, and machine-making industries,
        as Marchmont and Morningside.
        of learning and culture. The University of Edinburgh has made
        outstanding contributions to various fields. The Edinburgh
        International Festival (held annually since 1947) is acknowledged as
        Nationalism never completely disappeared, however, and in
        nationalists were in disarray when a referendum was defeated, and
        Stone of Destiny was returned to Scottish soil in 1996 — 700 years
        The general election of May 1997 proved to be a turning
        referendum on Scottish devolution. This took place in September 1997,
        Political power thus returned to Edinburgh after nearly 300
        Scottish people.
### Example 2

      grep -v "it" chZ.txt

        See also Cholos; Pachucos
        Zozobra
        See also El Kookoóee; Santa Fe Fiesta

 In these examples, I have used the -v option on grep. The -v option flips the way grep works so that it finds lines that do not contain the given word rather than do contain it. In the output of the examples, I have shown which liines in the given files do not contain the words "the" and "it" respectively. This option is useful generally because it allows the operation of grep to be flipped rather than having a completely new command. 
 
## Option 2: -c

### Example 1

     grep -c "Chicano" chZ.txt

        2

### Example 2

     grep -c "Japan" HistoryJapan.txt

        101

The -c option counts the number of lines that contains the given word. In the examples, "Chicano" is used in 2 lines in chZ.txt and "Japan" is used in 101 lines in HistoryJapan.txt. This is useful if the user wants to see the frequency of certain words without having to read the document. 

## Option 3: -r

### Example 1
      grep -r "Almancil" written_2
          written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt:The small crossroads town of Almancil has shops, cafés, and businesses, many of which are dedicated to serving English expatriates. But the town, of modest interest itself, is best known for what lies in its vicinity. Many of these ex-pats live just a few miles south on the coast, and it is here that two of the Algarve’s most luxurious and exclusive resorts are found. Surprisingly, given their status, neither Vale do Lobo nor Quinta do Lago are well sign-posted off the main road.    
          written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt:Back toward Almancil is one of the Algarve’s top attractions, but if you’re not looking closely, it’s easy to miss. About 16 km (10 miles) west of Faro, a simple white church stands out on a small hill overlooking the thundering highway. A sign simply says “S. Lourenço” — indicating the turn-off to São Lourenço do Matto (Church of St. Lawrence of the Woods). Inside is one of the most extraordinary displays of azulejo design you’ll ever see. Every square inch of the Baroque, 15th-century church — its walls, vaulted ceiling, and cupola — is covered with hand-painted, blue-and-white ceramic tiles. Most date from the early 18th century and depict biblical scenes detailing the life of St. Lawrence, born across the border in Huesca, Spain. The only element of the church not blue-and-white is the carved, gilded altar. The ensemble is a stunning 
          sight, not to be missed.
          written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt:Loulé, north of Almancil, is a regional produce center with a large Saturday market, known for its leather, lace, and copper goods. Loulé is a prosperous town with an ambitious, modern boulevard complete with outdoor cafés that are jam-packed on market day. Coach parties come from far and wide to shop at the colorful, bustling market.
          written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt:The small crossroads town of Almancil has shops, cafés, and businesses, many of which are dedicated to serving English expatriates. A few miles south on the coast are two of the Algarve’s most luxurious and exclusive resorts, Vale do Lobo and Quinta do Lago.
          written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt:Back toward Almancil is one of the Algarve’s top attractions. About 16 km (10 miles) west of Faro, a simple white church stands out on a small hill overlooking the thundering highway. A sign simply says “S. Lourenço” — indicating the turn-off to São Lourenço do Matto (Church of St. Lawrence of the Woods). Inside is one of the most extraordinary displays of azulejo design you’ll ever see. Every square inch of the Baroque, 15th-century church — its walls, vaulted ceiling, and cupola — is covered with hand-painted, blue-and-white ceramic tiles. Most date from the early 18th century and depict biblical scenes detailing the life of St. Lawrence. The ensemble is a stunning sight, not to be missed.
          written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt:Loulé, north of Almancil, is a prosperous town known for its leather, lace, and copper goods. Tour groups come from far and wide to shop at the colorful, bustling market. Just below the permanent market halls on the main Praça da República, you’ll find a well-preserved section of the medieval castle walls (which were much damaged by the 1755 earthquake). Also worth visiting are the Igreja Matriz (São Clemente), a 13th-century Gothic church with 18th-century azulejo tiles; the Convento da Graça, with a terrific Manueline portal; and Ermida de Nossa Senhora da Conceição, a small church prized for its Baroque altar and ceramic tiles.
      
### Example 2
      grep -r "David G. Farragut" written_2
          written_2/travel_guides/berlitz2/NewOrleans-History.txt:In April 1862, a Union naval force led by David G. Farragut capitalized on Confederate unpreparedness and penetrated the defenses of New Orleans. Despite localized opposition, within a week, the Union flag was raised over the city. It announced a military occupation destined to endure beyond the Civil War (or War between the States, as it is known in the south) into the Reconstruction period — for a total of 14 bitter years. The reconstruction of New Orleans began in 1879, when the 
          jetties were built to speed the flow of the Mississippi near its mouth. This improved navigation and returned the port to a position of strength. New railway lines linked the city with the rest of the United States.



## Option 4: -mmin

### Example 1
      [cs15lwi23aul@ieng6-202]:written_2:361$ find -mmin -10
      ./non-fiction/OUP/Castro/chM.txt
      ./non-fiction/OUP/Kauffman
      ./non-fiction/OUP/Kauffman/ch1.txt
      ./non-fiction/OUP/Kauffman/chQ.txt
      ./non-fiction/emptyfile2.txt
      ./travel_guides/berlitz2/Bahamas-WhatToDo.txt
      ./travel_guides/berlitz2/Poland-History.txt
      ./lab5
      ./lab5/emptyfile.txt
      
### Example 2
      [cs15lwi23aul@ieng6-202]:written_2:363$ find -maxdepth 2 -mmin +120
      .
      ./non-fiction
      ./non-fiction/OUP
      ./travel_guides
      ./travel_guides/berlitz2
      ./travel_guides/emptyDirectory
      ./-k
      
The -mmin option finds all files/directories that have been modified within the given time frame. Inputting a number after -mmin restricts the search to files that have been modified that number of minutes ago. Adding the +/- modifier give the command a range of times to look through, + being the given time and longer and - being the given time and less. In these examples, I have modifed specific files in the last 10 minutes and they are outputted in the first command while the rest I left untouched. This is useful if you are working on a shared directory and you want to know which files have been modified recently or which ones have not been modified recently.


All information was found at: https://man7.org/linux/man-pages/man1/find.1.html
