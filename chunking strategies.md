- A good chunking strategy is to use smaller chunks for embedding and an expanded window for the LLM
- simplest approach is to use fixed-size chunking.
  -   CharacterTextSplitter(separator = "\n\n", chunk_size = 1000, chunk_overlap = 100, length_function = len, is_separator_regex = False)
  -   split recursively by the number of characters until the resulting chunks are small enough , RecursiveCharacterTextSplitter(
      chunk_size = 100, chunk_overlap = 20, length_function = len,  is_separator_regex = False)
  -   For both of these strategies, however, you need to determine the chunk size, and it’s often unclear how to do that in a way that results in the best outcome.
- ParentDocumentRetriever
  -   the chunking is performed with smaller chunks, but the link to the original (parent) document is maintained, so that larger chunks surrounding the matching piece of text are available as input to the LLM summarization step.
  -   LangChain’s ParentDocumentRetriever and LLamaIndex’s SentenceWindowNodeParser.
