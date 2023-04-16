#ScorpioHead(27 February 2022, Scorpio &amp; SMILES)
##SMILES
###a spec for structure

SMILES is a standard format for specifying the structure of compounds.

Scorpio has partial support for SMILES.  

!!Scorpio
##Molecule
compound: CC(=O)NCCC1=CNC2=C1C=C(OC)C=C2
caption: Melatonin
:A: at: 121,117
:B: at: 168,116
:C: at: 181,163
:D: at: 190,70
:E: at: 238,60
:F: at: 283,73
:G: at: 289,121
:H: at: 253,153
:I: at: 275,201
:J: at: 324,186
:K: at: 324,140
:L: at: 360,118
:M: at: 400,144
:N: at: 435,117
:O: at: 474,146
:P: at: 399,183
:Q: at: 365,209
boxed: 250
!!Markdown

You can #NUTC(specify a compound) instead of giving the label and links specification, and when you next view the spec, the compound will have been expanded out to list all its labels.
#[
You could use a spec consisting of just these two lines:
<pre class='raw'>

&#35;&#35;Molecule<br>compound: CC(=O)NCCC1=CNC2=C1C=C(OC)C=C2
</pre>
or these two:
<pre class='raw'>

&#35;&#35;Molecule<br>compound: O=C(O)CC(O)C(=O)O
</pre>
The 'compound' line would disappear from the spec, and be replaced by a list of labels.  

#Rock(The SMILES feature is not complete yet.  There's plenty more to do.  The automatic layout of the molecule is currently disabled.  The connections are made per the SMILES spec, but you need to drag the labels into position.)
#]
