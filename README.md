# GD_Final_Project

# Relative clauses in Spanish
# A short description of the phenomenon
Relative clauses are widely spread in different languages, Spanish being one of them. Relative clauses are subordinated clauses that include more specified information about a noun of the main clause (cf. Rathsam & Schleyer 2016:275). There are different types of relative clauses but every type gets introduced with either a relative pronoun, a relative adverb or a relative companion. Within these different types different pronouns, adverbs and companions are possible (cf. Rathsam & Schleyer 2016:277). Some examples are illustrated in the following:
There are different relative pronouns in Spanish, for example que, quien and cual. The relative pronoun que is the same for male and female. Quien is the singular version of that relative pronoun but there is also the plural version of it which would be quienes (cf. Rathsam & Schleyer 2016:53). 
Examples for different relative adverbs in Spanish are donde and como. They do not differ between different gender and number.   
There are also relative companions in Spanish. Examples are cuyo and cuya. While cuyo is the male version of the relative companion, cuya is the female version of it. In addition, they can also be plural which would be cuyos for male and cuyas for female (cf. Rathsam & Schleyer 2016: 55). 
The basic order of the relative clause in Spanish is: relative pronoun/adverb/companion, subject, verb, addition (cf. Rathsam & Schleyer 2016: 277). It has to be noticed here that the subject can be omitted in Spanish since the ending of the verb already entails the person who is meant. Therefore, the subject can be empty (cf. Rathsam & Schleyer 2016:42). 

# Why I chose it
As already explained earlier relative clauses follow a regular pattern (get introduced with a relative pronoun/adverb/companion and so on). Thus, it seemed to be a good foundation to work with and to incorporate that pattern to build up the grammar. I didn´t choose Spanish because of a specific reason. Since I had Spanish in school it seemed to be a good idea because I still have some knowledge about that language. 

# Implementation approach and design
Test-suite:
I started by creating a test-suite which at first was filled with simple sentences. Then I started to expand the sentences by adding e.g. adjectives, adverbs and prepositions to make the sentences more complex. Especially adjectives differ between Spanish and English since in Spanish the adjective is mostly placed behind the noun and not in front of it as it would be the case in English (cf. Rathsam & Schleyer 2016:70). Of course, all of the sentences in the test-suite include a variety of relative pronouns/adverbs/companions. I also made sure that the sentences have different verbs regarding the required arguments (intransitive, transitive, ditransitive). In addition, I chose different types of determiners to illustrated that Spanish differs regarding determiners between male and female, definite and indefinite (cf. Rathsam & Schleyer 2016: 20). Something else to notice is that for example in comparison to German there is no need for a comma in Spanish relative clauses (cf. Rathsam & Schleyer 2016: 275). To summarize, I choose sentences with different elements to show some variation.  The sentences of the test-suite are illustrated in the following:

El 	            chico	      que	    habla
the.MASC.SG.DEF	boy.SG.NOM	who.RP	talk.3SG.PRES
‘The boy who talks.’ 

La	            mujer	        que	    canta	        bien
the.FEM.SG.DEF	woman.SG.NOM	who.RP	sing.3SG.PRES	good
‘The woman who sings good.’ 

El	            coche	      antiguo	que	    hace	        ruidos	      raros
the.MASC.SG.DEF	car.SG.NOM	old	    who.RP	make.3SG.PRES	noise.PL.ACC	weird
‘The old car that makes weird noises.’ 

Lisa	        que	    presenta	        un	              tema	    muy	  interesante
Lisa.FEM.NOM	who.RP	present.3SG.PRES	the.MASC.SG.INDEF	topic.ACC	very	interesting
‘Lisa who presents a very interesting topic.’

La	            ciudad	  donde	    Carlos	        trabaja
the.FEM.SG.DEF	city.NOM	where.RA	Carlos.MASC.NOM	work.3SG.PRES
‘The city where Carlos works.’ 

El	            bar	    donde	    Marta	        desayuna	          siempre
the.MASC.SG.DEF	bar.NOM	where.RA	Marta.FEM.NOM	breakfast.3SG.PRES	always
‘The bar where Marta always has breakfast.’ 

Alberto	          quien	    decide	        la	            fecha
Alberto.MASC.NOM	who.RP.SG	decide.3SG.PRES	the.FEM.SG.DEF	Date.ACC
‘Alberto who decides on the date.’ 

Los	            amigos	      quienes	  pintan	        cuadros	        grandes
the.MASC.PL.DEF	friend.PL.NOM	who.RP.PL	paint.3PL.PRES	picture.PL.ACC	big.PL
‘Friends who paint big pictures.’

El	            chico	      cuyo	            padre	      vive	        con	    la	            hermana
the.MASC.SG.DEF	boy.SG.NOM	whose.RC.SG.MASC	father.NOM	live.3SG.PRES	with.PP	the.FEM.SG.DEF	sister
‘The boy whose father lives with the sister.’

Los	            duenos	  cuyos	            perros	ladran
the.MASC.PL.DEF	owner.PL	whose.RC.PL.MASC	dog.PL	bark.3PL.PRES
‘The owners whose dogs bark.’ 

La 	            hermana	      cuya	          amiga	            cocina
the.FEM.SG.DEF	sister.SG.NOM	whose.RC.SG.FEM	friend.SG.FEM.NOM	cook.3SG.PRES
‘The sister whose friend cooks.’

Sentences that should not parse:
Adjective in front of the object:

Lisa	      que	    presenta	        un	              interesante	tema
Lisa.FEM.NOM	who.RP	present.3SG.PRES	the.MASC.SG.INDEF	interesting	topic.ACC

Two relative markers (doesn´t make much sense but to show that the implemented or in the grammar works):
El            chico	      que	    donde	    habla
the.MASC.SG.DEF	boy.SG.NOM	who.RP	where.RA	talk.3SG.PRES

Wrong determiner:
La	          amigos	            quienes	  pintan	        cuadros	        grandes
the.FEM.PL.DEF	friend.MASC.PL.NOM	who.RP.PL	paint.3PL.PRES	picture.PL.ACC	big.PL

Missing argument:
Alberto	        quien	    decide
Alberto.MASC.NOM	who.RP.SG	decide.3SG.PRES


Wrong punctuation:
Alberto	          quien	    decide	        la	            fecha	    !
Alberto.MASC.NOM	who.RP.SG	decide.3SG.PRES	the.FEM.SG.DEF	Date.ACC	!
‘Alberto who decides on the date!’ 


Grammar:
The rules of my created grammar in more detail from top to bottom is illustrated in the following. The NP consists of a noun or a pronoun and multiple optional elements namely determiner, AP and ADVP since these are not necessarily required. Since the relative clause gets introduced with a relative pronoun, relative adverb or a relative companion I chose to implement it in the grammar with the curly brackets and the |. The grammar continues with a NP in front of the V which is the subject of the relative clause and has the case marking nominative. The NP behind the V is considered to be the object and has the case marking of accusative. But also, the NP in both cases is not obligatory due to the subject that doesn´t necessarily need to be filled because of the verb that already contains that information and also an object is not necessarily required.  The grammar continues with another optional object which is required when dealing with a verb that is ditransitive. An optional ADVP is followed by an optional PP which is in the form of con since the PP in my test-suite contains the preposition con. 
Within my grammar relative adverbs/pronouns/companions are very important since the grammar is about relative clauses. Thus, these are explained in the following. The RAP, RAP and RCP consist of the proper relative pronoun, adverb or companion. These also are labelled as adverb, pronoun or companion so that they are labelled as those within the f-structure. 
Within my grammar I used different templates. I used templates for certain patterns that appeared often, for example the template for count nouns and names. I also used the templates for intransitive, transitive and ditransitive verbs. Most of the used templates are from grammars that we already had in the seminar but I also created new templates, for example for the relative companions.
For the OT-Marks I used the already existing common-template file. I chose the OT-Mark for the Period because the period at the end of the sentence is not necessarily required but preferred. For most of the sentences in the test-suite there is only one possible solution, therefore no further restrictions or OT-Marks are needed.

# Challenges that remain
The sentences contain of a main clause and a subordinate, relative clause. Therefore, two subjects, one of the main clause and one of the relative clause, are present. I struggled with implementing the subject of the relative clause. Thus, even though labelling the subject of the relative clause as nominative was no problem, labelling the subject as a subject and not as an object did not work out. 

# Files I have submitted and their function
I submitted, in addition to this readme file, three files which is the grammar, the test-suite and the common-template file. The grammar includes all the rules, templates and the lexicon of my created grammar that deals with relative clauses in Spanish. The test-suite includes all the test sentences to check whether the created grammar works or not. The common-template mark is needed for the OT-Marks. 

# A link to my GitHub repository
https://github.com/adinawellinger/GD_Final_Project

# Reference
Rathsam, Kathrin & Schleyer, Jochen. 2016. Spanische Grammatik. Berlin: Cornelsen Verlag.
