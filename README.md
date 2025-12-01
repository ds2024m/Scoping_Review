# Scoping_Review
Scoping Review Files

Considering Methodological transparency & reproducibility, following there are descriptions of the search strings with the corresponding timestamps:

**Scopus**

Fields searched: Title, Abstract, Keywords
Filters: English; Document types = Article, Book Chapter, Conference Paper; Subject Area = Computer Science
Search string:
TITLE-ABS-KEY ( "sentiment" OR "opinion mining" OR "affective" OR "affection" OR "affections" ) AND TITLE-ABS-KEY ( "multimodal" OR "multimodality" ) AND TITLE-ABS-KEY ( "summarization" OR "summarize" OR "skimming" OR "abstraction" ) AND ( LIMIT-TO ( DOCTYPE , "ar" ) OR LIMIT-TO ( DOCTYPE , "cp" ) OR LIMIT-TO ( DOCTYPE , "ch" ) ) AND ( LIMIT-TO ( SUBJAREA , "COMP" ) ) AND ( LIMIT-TO ( LANGUAGE , "English" ) )
Timestamp created file: 13 de março de 2025, 13∶58∶27
Timestamp modified file: 14 de fevereiro de 2025, 14∶35∶14

**ACM**
Search field: Abstract
Search string:
(Abstract:(sentiment) OR Abstract:(opinion mining) OR Abstract:(affective) OR Abstract:(affection) OR Abstract:(affections)) AND  (Abstract:(multimodal) OR Abstract:(multimodality)) AND (Abstract:(summarization) OR Abstract:(summarize) OR Abstract:(skimming) OR Abstract:(abstraction))
Timestamp created file: 13 de março de 2025, 13∶58∶27
Timestamp modified file: 14 de fevereiro de 2025, 14∶52∶04

**Science Direct**
Fields searched: Title, Abstract, Keywords
Filters: Research articles, Book chapters
Limitation: Max 8 Boolean operators per field → combined terms to avoid information loss.
Search string: ( "sentiment analysis" OR "opinion mining" OR "affective computing" OR "sentiment classification") AND ( "multimodal" OR "multimodality") AND ( "summarization"  OR "summarize" OR "skimming" OR "abstraction") --> This search string produces an error "Use fewer boolean connectors (max 8 per field)"
After search using different combinations of string, it was used this string without losing content: ( "sentiment" OR "affective" OR "opinion mining"  OR "affection") AND ( "multimodal" OR "multimodality") AND ( "summarization"  OR "skimming" OR "abstraction")
Filters: article type = research, book chapter
Timestamp created file: 13 de março de 2025, 13∶58∶27
Timestamp modified file: 14 de fevereiro de 2025, 14∶55∶44

**IEEE**
Search field: All Metadata
Search string: (((("All Metadata":"sentiment") OR ("All Metadata":"opinion mining") OR ("All Metadata":"affective") OR ("All Metadata":""affection"") OR ("All Metadata":"affections")) AND (("All Metadata":"summarization") OR ("All Metadata":"summarize") OR ("All Metadata":"skimming") OR ("All Metadata":"abstraction"))) AND (("All Metadata":"multimodal") OR ("All Metadata":"multimodality")))
Timestamp created file: 13 de março de 2025, 13∶58∶27
Timestamp modified file: 14 de fevereiro de 2025, 15∶00∶20

**ACL**
Method: Custom code to search in Title and Abstract
Timestamp download file: 13 de fevereiro de 2025, 09∶57∶40
The ACL Anthology does not provide an advanced search interface that allows filtering by both title and abstract. Therefore, a custom Python script was used to identify relevant studies. The script processed the full ACL Anthology BibTeX export (anthology_abstracts.bib), which contains metadata including title and abstract fields. Each entry was converted to lowercase and automatically screened for predefined keyword groups corresponding to sentiment/opinion analysis, multimodality, and summarization.
Three keyword groups were applied:
Sentiment / Opinion / Affective: “sentiment”, “opinion mining”, “affective”, “affection”, “affections”
Multimodality: “multimodal”, “multimodality”
Summarization: “summarization”, “summarize”, “skimming”, “abstraction”
A publication was considered only if it contained at least one keyword from each of the three groups in its title or abstract. Matching was performed using a bitwise operation that required the presence of all three conceptual components. 
Publications meeting the criteria were exported to a separate BibTeX file (resultado.bib) for screening.
No language or year restrictions were applied.

**Additional Comments:**
Before reaching this final search string and consequently the final set of records, an iterative process took place, involving searches and analysis of the articles retrieved. This process is not included in the updated files available in this repository.
This project also includes original BibTeX files from February 2025, as well as files exported from the study-selection process conducted using the Parsifal website (a systematic review tool available at https://parsif.al/), which supported this phase of the work. The Parsifal exports contain details on the 2024 BibTeX files that were imported, along with the newly added files from 2025. The platform was also used to help identify and remove duplicate articles.


