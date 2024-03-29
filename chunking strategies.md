- https://github.com/FullStackRetrieval-com/RetrievalTutorials/blob/main/5_Levels_Of_Text_Splitting.ipynb
  -  Level 1: Character Splitting - Simple static character chunks of data
  -  Level 2: Recursive Character Text Splitting - Recursive chunking based on a list of separators
  -  Level 3: Document Specific Splitting - Various chunking methods for different document types (PDF, Python, Markdown)
  -  Level 4: Semantic Splitting - Embedding walk based chunking
  -  Level 5: Agentic Splitting - Experimental method of splitting text with an agent-like system. Good for if you believe that token cost will trend to $0.00
  -  ***Bonus Level:*** Alternative Representation Chunking + Indexing - Derivative representations of your raw text that will aid in retrieval and indexing 
- A good chunking strategy is to use smaller chunks for embedding and an expanded window for the LLM
  - using the same big text chunk for retrieval and synthesis is not optimal when there is a lot of filler text in the text chunk.
  - small-to-big-retrieval
     -  concept is to use smaller text chunks during the retrieval process and
     -  subsequently provide the larger text chunk to which the retrieved text belongs to the large language model.
     -  Smaller Child Chunks Referring to Bigger Parent Chunks: Fetch smaller chunks during retrieval first, then reference the parent IDs, and return the bigger chunks.
     -  Sentence Window Retrieval: Fetch a single sentence during retrieval and return a window of text around the sentence.
- simplest approach is to use fixed-size chunking.
  -   CharacterTextSplitter(separator = "\n\n", chunk_size = 1000, chunk_overlap = 100, length_function = len, is_separator_regex = False)
  -   split recursively by the number of characters until the resulting chunks are small enough , RecursiveCharacterTextSplitter(
      chunk_size = 100, chunk_overlap = 20, length_function = len,  is_separator_regex = False)
  -   For both of these strategies, however, you need to determine the chunk size, and it’s often unclear how to do that in a way that results in the best outcome.
- ParentDocumentRetriever
  -   the chunking is performed with smaller chunks, but the link to the original (parent) document is maintained, so that larger chunks surrounding the matching piece of text are available as input to the LLM summarization step.
  -   LangChain’s ParentDocumentRetriever and LLamaIndex’s SentenceWindowNodeParser.
- “Content-aware” chunking.
  -   Set of methods for taking advantage of the nature of the content we’re chunking and applying more sophisticated chunking to it.
  -   parsing PDFs along with hierarchical layout information
      -  Identifying sections and subsections, along with their respective hierarchy levels.
      -  Merging lines into coherent paragraphs.
      -  Establishing connections between sections and paragraphs.
      -  Recognizing tables and associating them with their corresponding sections.
      -  Handling lists and nested list structures with precision.
- [Chunking Strategies](https://www.linkedin.com/pulse/prompt-engineering-chunking-strategies-ravi-naarla/)
