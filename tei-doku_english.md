# TEI Documentation

**Date:** 06/03/2024

## Overview
### Basic Structure

Every token (each segment) in the text has a specific function defined by the attribute `seg type="..."`. This attribute allows for arbitrary segmentation of the text below the 'chunk' level.

A segment can have two main functions:
1. It can be a word or a punctuation mark.
2. These functions are defined by the following types:
   - `seg type="token"`: Represents a word or a token unit.
   - `seg type="pc"`: Represents a punctuation character.

### Token Attributes

If the segment does not have the attribute type `pc`, each token can possess the following attributes:

| Attribute   | Function | Example |
|-------------|----------|---------|
| `xml:id`    | (identifier) Provides a unique identifier for the element carrying the attribute | `xml:id="HZU_161308032501_9"` |
| `lemmaRef`  | References a definition of the lemma for the word | `lemmaRef="6301"` |
| `meaningRef`| References the meaning of the word | `meaningRef="9929"` |
| `pos`       | (part of speech) Indicates the part of speech assigned to a token | `pos="VRB"` |
| `wordRef`   | References the word in a dictionary or lexicon | `wordRef="101732"` |

    

### Structural Elements

| Element      | Description | Example |
|--------------|-------------|---------|
| `teiHeader`    | Placeholder for header information | ... |
| `body`         | Contains the entire body of a single text unit, excluding front or back matter | `<tei:body>` |
| `p`            | (paragraph) Marks paragraphs in prose | `<tei:p resp="Generated by Export-Script">` |
| `div`          | (text division) Contains subdivisions of a text | `<tei:div resp="Generated by Export-Script">` |
| `head`         | (heading) Contains headings such as section titles or list headings | `<tei:head>` |
| `l`            | (verse line) Contains a single line of verse | `<tei:l n="50050">` |
| `cb`           | (column beginning) Marks the start of a new column on a multi-column page | `<tei:cb n="1" type="manuscript"/>` |
| `pb`           | (page beginning) Marks the start of a new page in a paginated document | `<tei:pb n="5"/>` |
| `lb`           | (line beginning) Marks the start of a new line in a text | `<tei:lb n="1"/>` |
| `lg`           | (line group) Contains verse lines as a formal unit, such as a stanza | `<tei:lg type="stanza" n="1">` |
| `num`          | (number) Contains a number in any form | `<tei:num>` |
| `caesura`      | Marks a point where a metrical line may be divided | `<tei:caesura/>` |
| `supplied`     | Signifies text supplied by the transcriber or editor | `<tei:supplied>` |
| `hi`           | (highlighted) Marks a word or phrase as distinct from the surrounding text | `<tei:hi rend="initial">` |

### Additional Information

| Date Attributes | Description | Example |
|-----------------|-------------|---------|
| Year            | type="year" | `<tei:note type="year" n="1292"/>` |
| Date            | type="date" | `<tei:note type="date" n="224"/>` |

| Attributes | Description | Examples |
|------------|-------------|----------|
| `type`       | Characterizes the element using a classification scheme | song, number, recipe, chapter, stanza, sermon, colophon, deed, folio, manuscript, edition, year, date, volume |
| `rend`       | Indicates the rendering or presentation of the element in the source text | initial, upper_case, upper_case_first_letter, bold, italic |
| `n`          | Provides a number or label for an element, which may not be unique within the document | Numerical values |


