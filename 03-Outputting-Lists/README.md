# FlatList

*FlatList* replaces *ScrollView* with a more performant option for lists.

FlatList has two crucial properties:

- **data**: this is the data that we want to pass into our FlatList, this usually points to an array of data.

- **renderItem**: this is a function that returns what we want *FlatList* to render given the current item in the data that we provided. The item passed in to the array has three available properties: item (data), index, and seperator. We usually only care about the item

- **keyExtractor**: takes a function that tells *FlatList* what to use for our key. The function takes two arguments, the item and the index. Then we have to return a key. By default, key extractor looks for item.key. If we are providing something other than a key, we can specify the unique identifier that we want to use for a key.