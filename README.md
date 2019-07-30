# Hungarian-morphological-analyzer
This is a [foma](https://fomafst.github.io)-based morphological analyzer for Hungarian, which I developed under the instruction of [Dr. Mans Hulden](http://verbs.colorado.edu/~mahu0110/) during the 2016 San Sebastián (Donostia) NLP summer school "[Codefest](http://www.ehu.eus/ehusfera/ixa/2016/04/07/codefest-summer%C2%ADlab-aims-to-revitalise-resource-%C2%ADscarce-language-donostia-july-4-8/)."

The morphological analyzer consists of two parts: a lexicon (HUN.lexc) and a foma script (HUN.foma), the latter including a number of alternation rules (or rewrite rules) and the subgrammar composition. Thanks to the bidirectional feature of finite-state networks, this linguistic tool is simultaneously a word analyzer (i.e., it can analyze an inflected Hungarian word into its morphological components) and a word generator (i.e., it can convert an abstract morphological representation into an orthographically correct Hungarian word).

For example:

(1) Word analysis: _ablakon_ => `ablak[N][SG][SUP]` (i.e., _ablakon_ is the superessive case form of the singular noun _ablak_ 'window', which literally means 'on [the] window') 

(2) Word generation: `fekete[ADJ][PL]` => _feketék_ (i.e., the plural form of the adjective _fekete_ 'black' is _feketék_)

To run the morphological analyzer, you need to install foma, a finite-state toolkit designed for natural language processing developed by Dr. Mans Hulden. For installation instruction see its [GitHub repo](https://github.com/mhulden/foma/tree/master/foma).

After installing foma, simply enter the `foma` environment in the terminal and run `source HUN.foma` (within the directory where you have downloaded the foma scripts) to compile. When the compilation is completed, either enter the `up` mode and do word analyses or enter the `down` mode and do word generation.

The morphological analyzer in its current state has a basic lexicon of 9654 nouns, 2238 verbs, and 1637 adjectives. It may very well make occasional mistakes as the summer school was only five days and I have not had time to further work on the project since then. But I am likely to return to it in the future, so any suggestions are welcome! Köszönöm szépen!
