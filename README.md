# MEDG website (version 2022)

* For any questions, please contact Wei-Hung Weng (ckbjimmy {AT} mit {DOT} edu)
* Latest update: May 28, 2022

## Instructions to update the content

* Most content can be updated via the `.md` files in the `docs` folder except for the `news` in the `index.html`.
* Please update via the files in this github repo
<!-- * Please copy the files into `/afs/csail.mit.edu/group/medg/www/data` to display the website under the CSAIL domain. -->

## Some instructions for updating the group bibliography

* Create your own `.bib` file in the folder `bib`, then add `<bibtex src="bib/[YOUR_BIB_NAME].bib"></bibtex>` in the `<head>` of `publications.html`. Just need to do this once.
* The easiest way to get your full bib data is [exporting them from
  Google
  Scholar](https://www.ndsu.edu/fileadmin/digitalmeasures/DM_Training_Materials/BibTex_Exports_from_Google_Scholar.pdf). However, 
  you may want to assure that Google Scholar includes the papers you
  want to display and then exclude those papers Google Scholar has
  errorneously included. 
* For the bib entry, please add `pmid`, `pmcid`, `url` if
  possible. The code will parse these attributes and display them on
  the website. 
* If you wish, you may also add the `tags` attribute. The strings in
  the `tags` can be searched as a filter. 
* The easiest way to get all of your publications is to export the
  bibtex file from Google Scholar. However, please remember to exclude
  the publications not belonging to you (GScholar sometimes did this
  incorrectly). You may manually add the `pmid`, `pmc`, `url`, `tags`
  after exporting the bibtex file. 
* Please do not include punctuations such as `:` or `=` or `+`  in the
  bibentry key. It will result in problems displaying the  paper/bib
  because of some vagery in the javascript bibtex parser. 
* An example of the above attributes:

```
@article{weng2017medical,
  title={Medical subdomain classification of clinical notes using a machine learning-based natural language processing approach},
  author={Weng, Wei-Hung and Wagholikar, Kavishwar B and McCray, Alexa T and Szolovits, Peter and Chueh, Henry C},
  journal={BMC medical informatics and decision making},
  volume={17},
  number={1},
  pages={155},
  year={2017},
  publisher={BioMed Central},
  pmid={29191207},
  pmc={PMC5709846},
  url={https://bmcmedinformdecismak.biomedcentral.com/articles/10.1186/s12911-017-0556-8},
  tags={machine learning, NLP, classification, ontology}
}
```

* For the thesis entry (`MEDG-theses.bib`), it would be better to include the following attributes as they will be used and displayed:

```
@phdthesis{Ghassemi2017hq,
	Address = {Cambridge, MA},
	Author = {Ghassemi, Marzyeh},
	Department = {EECS},
	Month = {Jun},
	Reader = {Guttag, John and Celi, Leo Anthony G},
	School = {MIT},
	Supervisor = {Szolovits, Peter},
	Title = {Representation Learning in Multi-dimensional Clinical Timeseries for Risk and Event Prediction},
	Type = {PhD Thesis},
	Url = {https://dspace.mit.edu/handle/1721.1/112389},
	Year = {2017}
}
```

* The bibtex parser is inherited and modified from `https://github.com/pcooksey/bibtex-js`.
