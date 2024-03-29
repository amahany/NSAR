# Negation and Speculaiton in Arabic Review (NSAR)

NSAR is the first pubicaly available Arabic review corpus annotated with negation and speculation. It includes around 3K review sentences from three well-known Arabic corpora. These sentences cover review for various topics, such as products and resturants. The below table show the distribution of the sentences for each topic.
| Topic | Books | Touristic Places | Hotels | Products | Restaurants | Software | 
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | 
| No. of Sentences | 1040 | 108 | 74 | 916 | 473 | 400 |

Webanno tool is used for the annotation process where 29% and 4% of the corpus includes negated and speculated sentences respectively. The annotated sentences are written in TSV file format as in the corpus directory. 

To read the annotated sentences, there is a need to install web-anno-tsv 0.0.1 python package using `pip install web-anno-tsv`. This is a sample python script to read LABR TSV file.

```
from web_anno_tsv import open_web_anno_tsv

labr = 'corpus/LABR.tsv'

with open_web_anno_tsv(labr) as f:
    for i, sentence in enumerate(f):
        print(f"Sentence {i}:", sentence.text)
        for j, annotation in enumerate(sentence.annotations):
            print(f'\tAnnotation {j}:')
            print('\t\tText:', annotation.text)
            print("\t\tLabel:", annotation.label)
```
### Citation

1. Mahany, A.; Khaled, H.; Elmitwally, N.S.; Aljohani, N.; Ghoniemy, S. Annotated Corpus with Negation and Speculation in Arabic Review Domain: NSAR. IJACSA. 2022, 13, 7. https://doi.org/10.14569/IJACSA.2022.0130706
2. Mahany, A.; Khaled, H.; Elmitwally, N.S.; Aljohani, N.; Ghoniemy, S. Negation and Speculation in NLP: A Survey, Corpora, Methods, and Applications. Appl. Sci. 2022, 12, 5209. https://doi.org/10.3390/app12105209
