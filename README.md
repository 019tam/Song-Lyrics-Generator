# Song-Lyrics-Generator

 IMusic Maker
Team Members: Sanjana Prakash,  Lingyi You
Ningke Hu, Tamara Prabhakar, Ruijie Cao

Our program is called IMusic Maker, a smart software that generates a brief song based on the user’s desired genre input. In order to run the program, please make sure you have the following in the correct project folder (and please make sure the file path matches): 
Our main function is in MusicMaker class. Run MusicMaker to generate a song by following the steps shown on the console.
“love-word”: this document contains our trainer set of the love-related words in order to classify the song as a love song or not 
“newlyrics.csv: This file contains our database of nearly 500 songs 
“newlyrics2.csv”: This file is a smaller data set for testing in MusicMakerTest
“newlyrics3.csv”: This file is a smaller data set for testing in ClassifierTest
“testIDF.csv”: This file is a smaller data set for testing in IDFVisitorTest
“testTF.csv”: This file is a smaller data set for testing in TFVisitorTest
In order to use the IBM Watson Natural Language Understanding API:
 please be sure to include the following jar file, which can be downloaded here. Please add this under referenced libraries. 
To access the API, in the song class inside the getWatsonSentiment() method, we have included the API key which should look like this: .apiKey("lnDDRc588Zowp2dMdk391B4ON7UD045l3NmsUPZWHEHN") 
The endpoint URL has also already been set and it should look like this: 
naturalLanguageUnderstanding.setEndPoint("https://gateway-wdc.watsonplatform.net/natural-language-understanding/api");
Please note that there is a limit on the number of times the API can be used(100000 words per month for one API key). If the program is run several times within the month, the limit will run out (but hopefully this should not occur unless the program is run an excessive number of times)
If the API does run out, please email any group member for a new API key and URL.
At this point, you should be able to successfully run the program.
Clarification on one upgrade:
In the project design docs, we generate lyrics using only the most highly- ranked songs. However, to make full use of all of the songs in genre base, we mix sentences from highest scored songs, lowest scored songs and average scored songs. We generate part of lyrics from the top 10% scored songs to make sure the lyrics contain enough of the correct emotions designated by genre, while the rest of the lyrics are based on random selections from this genre.
