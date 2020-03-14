# Etunimitin

Weighted sampling based Finnish given name generator. Uses Finnish name data set from https://www.avoindata.fi/data/fi/dataset/none. Separated weighted selection for first given name and other given names.


## Configuration

The generation can be configured through the following query parameters

 - `amount`: Number of names generated per gender, default 3
 - `minLength`: Minimum number of characters in names
 - `maxLength`: Maximum number of characters in names
 - `popularity`: Weight given to name popularity, default 1
    - 1+: Popular names are given additional probability
    - 1: Names probability matches real world distribution
    - 0 – 1: Popular names have reduced probability
    - 0: All names have equal probability, regardless of real world distribution
    - 0-: Unpopular names appear even more often than popular names
 - `beginWith`: Characters that names should start in, note case sensitivity
 - `endWith`: Characters that names should end in

### Example
https://aeirola.github.io/etunimitin/?amount=4&beginWith=H&maxLength=6&popularity=0.5 will produce 4 names, starting with the letter H, which are at most 6 letters long and slightly less popular than the real world distribution.