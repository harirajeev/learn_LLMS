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
