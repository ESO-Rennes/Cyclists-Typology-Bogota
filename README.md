</head>

<body lang=FR link=blue vlink="#954F72" style='tab-interval:35.4pt;word-wrap:
break-word'>

<div class=WordSection1>

<p class=MsoNormal style='mso-margin-top-alt:auto;margin-bottom:12.0pt;
line-height:normal;background:white'><span lang=EN-GB style='font-size:12.0pt;
font-family:"Segoe UI",sans-serif;mso-fareast-font-family:"Times New Roman";
color:#1F2328;mso-ansi-language:EN-GB;mso-fareast-language:FR'>----- ENGLISH
VERSION -----<br>
<i>This work was carried out by&nbsp;<span class=SpellE><a
href="https://perso.univ-rennes2.fr/maelle.lucas">Maëlle Lucas</a></span> and&nbsp;</i></span><i><span
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:
"Times New Roman";color:#1F2328;mso-ansi-language:FR;mso-fareast-language:FR'><a
href="https://perso.univ-rennes2.fr/florent.demoraes"><span lang=EN-GB
style='mso-ansi-language:EN-GB'>Florent <span class=SpellE>Demoraes</span></span></a></span></i><i><span
lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'>&nbsp;at the CNRS ESO research unit in Rennes
(France), in March 2021 and updated in October 2024.</span></i><span
lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'><o:p></o:p></span></p>

<p class=MsoNormal style='margin-top:18.0pt;margin-right:0cm;margin-bottom:
12.0pt;margin-left:0cm;line-height:normal;mso-outline-level:2;background:white'><b><span
lang=EN-GB style='font-size:18.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'>Devising a cyclist’s typology from a household travel
survey and mapping the resulting profiles<o:p></o:p></span></b></p>

<p class=MsoNormal style='margin-bottom:12.0pt;line-height:normal;background:
white'><span lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'>This blog presents a method for devising a typology of
bike users based on a Household Travel Survey conducted in 2019 in Bogotá, and
available in&nbsp;</span><span style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:FR;
mso-fareast-language:FR'><a
href="https://www.simur.gov.co/encuestas-de-movilidad"><span lang=EN-GB
style='mso-ansi-language:EN-GB'>open data</span></a></span><span lang=EN-GB
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:
"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;mso-fareast-language:
FR'>. The method relies on Factorial Analysis of Mixed Data and Hierarchical
Agglomerative Clustering. The analysis combines sociodemographic
characteristics of 3,241 individuals and variables describing their mobility
practices. Maps showing the concentration of the places of residence and the
concentration of places of destination of the six bike users’ profiles are provided.
The method developed in R is replicable to other urban areas and other groups
of people using other travel modes.<o:p></o:p></span></p>

<p class=MsoNormal style='margin-bottom:12.0pt;line-height:normal;background:
white'><span lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'>This study is part of a PhD thesis developed by&nbsp;<a
href="https://perso.univ-rennes2.fr/maelle.lucas"><span class=SpellE>Maëlle</span>
Lucas</a>&nbsp;and also part of the activities of the&nbsp;</span><span
class=SpellE><span style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:FR;
mso-fareast-language:FR'><a href="https://modural.hypotheses.org/le-projet"><span
lang=EN-GB style='mso-ansi-language:EN-GB'>Modural</span><span lang=EN-GB
style='mso-ansi-language:EN-GB'> program</span></a></span></span><span
lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'>&nbsp;funded by the French National Research Agency.<o:p></o:p></span></p>

<p class=MsoNormal style='margin-top:18.0pt;margin-right:0cm;margin-bottom:
12.0pt;margin-left:0cm;line-height:normal;mso-outline-level:4;background:white'><b><span
lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'>Key words<o:p></o:p></span></b></p>

<p class=MsoNormal style='margin-bottom:12.0pt;line-height:normal;background:
white'><i><span lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'>cyclists; typology; daily mobility; household travel
survey; factor analysis, clustering, , R script</span></i><span
lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'><o:p></o:p></span></p>

<p class=MsoNormal style='margin-bottom:12.0pt;line-height:normal;background:
white'><span lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'>--&gt; Access to the&nbsp;</span><span
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:
"Times New Roman";color:#1F2328;mso-ansi-language:FR;mso-fareast-language:FR'><a
href="https://github.com/ESO-Rennes/Cyclists-Typology-Bogota/blob/main/ScriptTypoCyclistesAFDM_v8.Rmd"><b><span
lang=EN-GB style='mso-ansi-language:EN-GB'>R markdown script</span></b></a></span><span
lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'><br>
--&gt; Access to the&nbsp;</span><span style='font-size:12.0pt;font-family:
"Segoe UI",sans-serif;mso-fareast-font-family:"Times New Roman";color:#1F2328;
mso-ansi-language:FR;mso-fareast-language:FR'><a
href="https://htmlpreview.github.io/?https://github.com/ESO-Rennes/Cyclists-Typology-Bogota/blob/main/ScriptTypoCyclistesAFDM_v8.html"><b><span
lang=EN-GB style='mso-ansi-language:EN-GB'>HTML laid-out output</span></b></a></span><span
lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'><br>
--&gt; Access to the&nbsp;</span><span class=SpellE><span style='font-size:
12.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:"Times New Roman";
color:#1F2328;mso-ansi-language:FR;mso-fareast-language:FR'><a
href="https://github.com/ESO-Rennes/Cyclists-Typology-Bogota/raw/main/data.zip"><b><span
lang=EN-GB style='mso-ansi-language:EN-GB'>the</span></b><b><span lang=EN-GB
style='mso-ansi-language:EN-GB'> data processed in the script</span></b></a></span></span><span
lang=EN-GB style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;
mso-fareast-language:FR'><br>
<br>
<br style='mso-special-character:line-break'>
<![if !supportLineBreakNewLine]><br style='mso-special-character:line-break'>
<![endif]><o:p></o:p></span></p>

<p class=MsoNormal style='margin-bottom:12.0pt;line-height:normal;background:
white'><span style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:FR;
mso-fareast-language:FR'>----- VERSION FRANCAISE -----<br>
<i>Ce travail a été réalisé par&nbsp;</i></span><i><span lang=EN-GB
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:
"Times New Roman";color:#1F2328;mso-ansi-language:EN-GB;mso-fareast-language:
FR'><a href="https://perso.univ-rennes2.fr/maelle.lucas"><span lang=FR
style='mso-ansi-language:FR'>Maëlle Lucas</span></a></span></i><i><span
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:
"Times New Roman";color:#1F2328;mso-ansi-language:FR;mso-fareast-language:FR'>&nbsp;et&nbsp;<a
href="https://perso.univ-rennes2.fr/florent.demoraes">Florent <span
class=SpellE>Demoraes</span></a>&nbsp;au sein de l'unité de recherche CNRS ESO
à Rennes (France), en mars 2021 et mis à jour en octobre 2023.</span></i><span
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:
"Times New Roman";color:#1F2328;mso-ansi-language:FR;mso-fareast-language:FR'><o:p></o:p></span></p>

<p class=MsoNormal style='margin-top:18.0pt;margin-right:0cm;margin-bottom:
12.0pt;margin-left:0cm;line-height:normal;mso-outline-level:2;background:white'><b><span
style='font-size:18.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:
"Times New Roman";color:#1F2328;mso-ansi-language:FR;mso-fareast-language:FR'>Construction
d'une typologie de cyclistes à partir d'une enquête ménages déplacements et
cartographie des profils obtenus<o:p></o:p></span></b></p>

<p class=MsoNormal style='margin-bottom:12.0pt;line-height:normal;background:
white'><span style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:FR;
mso-fareast-language:FR'>Ce billet présente une méthode pour concevoir une
typologie d’usagers du vélo à partir d'une Enquête Ménages Déplacements menée
en 2019 à Bogotá, et disponible en&nbsp;<a
href="https://www.simur.gov.co/encuestas-de-movilidad">open data</a>. La
méthode repose sur une analyse factorielle de données mixtes et sur une
classification ascendante hiérarchique. L'analyse combine des caractéristiques
sociodémographiques de 3241 individus et des variables décrivant leurs
pratiques de mobilité. Des cartes montrant la concentration des lieux de
résidence et la concentration des lieux de destination des six profils de
marcheurs sont proposées. La méthode développée dans R est reproductible à
d'autres zones urbaines et à d'autres groupes de personnes utilisant d'autres
modes déplacement.<o:p></o:p></span></p>

<p class=MsoNormal style='margin-bottom:12.0pt;line-height:normal;background:
white'><span style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:FR;
mso-fareast-language:FR'>Cette étude fait partie d'une thèse de doctorat
menée par&nbsp;</span><span lang=EN-GB style='font-size:12.0pt;font-family:
"Segoe UI",sans-serif;mso-fareast-font-family:"Times New Roman";color:#1F2328;
mso-ansi-language:EN-GB;mso-fareast-language:FR'><a
href="https://perso.univ-rennes2.fr/maelle.lucas"><span lang=FR
style='mso-ansi-language:FR'>Maëlle Lucas</span></a></span><span
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:
"Times New Roman";color:#1F2328;mso-ansi-language:FR;mso-fareast-language:FR'>&nbsp;et
s'inscrit également dans les activités du&nbsp;<a
href="https://modural.hypotheses.org/le-projet">programme <span class=SpellE>Modural</span></a>&nbsp;financé
par l'Agence Nationale de la Recherche.<o:p></o:p></span></p>

<p class=MsoNormal style='margin-top:18.0pt;margin-right:0cm;margin-bottom:
12.0pt;margin-left:0cm;line-height:normal;mso-outline-level:4;background:white'><b><span
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:
"Times New Roman";color:#1F2328;mso-ansi-language:FR;mso-fareast-language:FR'>Mots
clés<o:p></o:p></span></b></p>

<p class=MsoNormal style='margin-bottom:12.0pt;line-height:normal;background:
white'><span class=GramE><i><span style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:FR;
mso-fareast-language:FR'>cyclistes</span></i></span><i><span style='font-size:
12.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:"Times New Roman";
color:#1F2328;mso-ansi-language:FR;mso-fareast-language:FR'> ; typologie ; enquête
ménages déplacements ; analyse factorielle, classification, Bogotá, R script</span></i><span
style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;mso-fareast-font-family:
"Times New Roman";color:#1F2328;mso-ansi-language:FR;mso-fareast-language:FR'><o:p></o:p></span></p>

<p class=MsoNormal style='mso-margin-bottom-alt:auto;line-height:normal;
background:white'><span style='font-size:12.0pt;font-family:"Segoe UI",sans-serif;
mso-fareast-font-family:"Times New Roman";color:#1F2328;mso-ansi-language:FR;
mso-fareast-language:FR'>--&gt; Accès au&nbsp;<a
href="https://github.com/ESO-Rennes/Cyclists-Typology-Bogota/blob/main/ScriptTypoCyclistesAFDM_v8.Rmd"><b>script
R <span class=SpellE>markdown</span></b></a><br>
--&gt; Accès à&nbsp;<a
href="https://htmlpreview.github.io/?https://github.com/ESO-Rennes/Cyclists-Typology-Bogota/blob/main/ScriptTypoCyclistesAFDM_v8.html"><b>la
sortie HTML</b></a><br>
--&gt; Accès aux&nbsp;<a
href="https://github.com/ESO-Rennes/Cyclists-Typology-Bogota/raw/main/data.zip"><b>données
traitées dans le script</b></a><o:p></o:p></span></p>

<p class=MsoNormal><span style='mso-ansi-language:FR'><o:p>&nbsp;</o:p></span></p>

</div>

</body>

</html>
