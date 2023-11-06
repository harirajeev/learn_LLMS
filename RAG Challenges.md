- challenge 1: chunking strategy
    - One solution involves the implementation of knowledge graphs, which I successfully applied for one of my clients, yielding highly effective results.
    - created an ontology for the documents for the company and then used LLM and code to convert that document into knowledge graph. I used neo4j as database
    - will give more rich context to the LLMs
    - At Unstructured we are building out some context aware chunking strategies such as chunking by title. The strategy can help keep contextually similar pieces together.
    - Additionally we also break down the document's hierarchy for more accurate results.
       - https://unstructured-io.github.io/unstructured/bricks/chunking.html
       - https://github.com/Unstructured-IO/unstructured/blob/main/unstructured/chunking/title.py

- challenge 2: Many of our documents have a hierarchical structure, with sections, subsections, and sub-subsections. To create robust embeddings, it's essential to convert this hierarchical structure into a flat structure.
    - filtering or even nested filtering https://qdrant.tech/documentation/concepts/filtering/#nested-key
    - convert hierarchical structured document to flat document

- challenge 3: documents could get updated. Hence correspondng embedding also needs to be updated. Need for metadata.
    - deduplication / versioning based on checksum
    - versioning of documents
    - Quadrnt - filter based on metadata of documents
    - new elements are available for search immediately after inserting/updating

- challenge 4 : query builder
    - sometimes one question has multiple subquestions which can be from content or out of context so multiquery , subquery and handling them via guardrails is one way 

- challebge 5: evaluation 
             - RAGAS
             - how to evaluate QA @ run time .... confidence score ?
             - 
- challenge 6: prompt management 
             - thru W&B
             - can it be at user level / client level

- challange 7: how to take feed back from users and improve answers

Complexity of Parsing PDFs
- Layout Complexity: PDFs can contain complex layouts, such as multi-column text, tables, images, and intricate formatting. This layout diversity complicates the extraction of structured data.
- Font encoding issues: PDFs use a variety of font encoding systems, and some of these systems do not map directly to Unicode. This can make it difficult to extract the text accurately.
- Non-linear text storage: PDFs do not store text in the order it appears on the page. Instead, they store text in objects that can be placed anywhere on the page. This means that the order of the text in the underlying code may not match the order of the text as it appears visually.
- Inconsistent use of spaces: In some PDFs, spaces are not used consistently or are not used at all between words. This can make it difficult to even identify word boundaries.
