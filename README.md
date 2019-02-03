# Gutenberg Paragraphs Local API

This project will provide the a local API for gutenberg books and paragraphs.

### Packages
This API uses numpy package. Also it is recomended to use python 3.5+ for memory control.

### Setting
 API needed two types of data. first gutenberg book's text which should be saved in the file named "<gutenberg_id\>.txt" and some metadata's: books_metadata.json, features_metadata.json, paragraphs.npy. you can set their paths in HP.py python code.
 
 ### Books Metadata
 the main methods for books metadata are get_books and get_books metadata. books metadata are in format of dictionary and includes gutenberg_id, title, authors, languages, bookshelves and has_text \(whether it has text or not\)
 
 ### Paragraph Metadata
 This API also provide  metadata about paragraphs: global_id, book_id, local_id \(in book\), is_analysed \(wether it is analysed by nltk or not\), number of sentences, number of words, number of token and ... . the basic metadata is in the format of numpy array. 
 
 ### local_id format V.S global_id format
 
 a given set of paragraphs \(id\) can have two system of database. First is global_id format which is a list of global_ids. Second is local_id format which categorize parapgraphs by books. it's a dictionary which keys are books_id and values are list of local_ids. this format is better for extracting text from data source. API works with these two formats. for further read explanations under methods.
 
 
 