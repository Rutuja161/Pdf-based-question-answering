#Pdf-based-question-answering

This is the research project for my master's in Data analytics. This aims to build a smart question-answering system for PDF files using BERT-based transformers.

##Approches:
- Question Answering System Using fine-tuned BERT base and BERT large for PDFs from the financial domain.
- Question Answering System Using SciBERT for PDFS from the scientific domain.
- Question Answering System Using Bio-clinicalBERT for PDFS from the biomedical domain.
- Question Answering System by fine-tuning DistillBERT on SQAuD dataset for PDFS from the financial domain.

##Challenges:
- BERT has a limitation of processing 512 tokens and the PDFs chosen were longer than the 512 token limit. The model worked fine for short paragraphs extracting accurate answers while it performed poorly for long documents containing complex texts. To overcome this, PDFs were split into chunks of 512 and then fed to the QA model to extract answers. 
- 
