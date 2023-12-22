#Pdf-based-question-answering

This repository hosts a collection of Question Answering Systems (QAS) tailored for PDF documents from distinct domains, namely financial, scientific, and biomedical. The systems are built using fine-tuned BERT base, BERT large, SciBERT, Bio-clinicalBERT, and DistillBERT models, offering specialized solutions for each domain. Additionally, the repository includes a comprehensive dataset creation process for each domain and a cross-domain evaluation to assess the models' generalization capabilities.

##Approches:
- Question Answering System Using fine-tuned BERT base and BERT large for PDFs from the financial domain.
- Question Answering System Using SciBERT for PDFS from the scientific domain.
- Question Answering System Using Bio-clinicalBERT for PDFS from the biomedical domain.
- Question Answering System by fine-tuning DistillBERT on SQAuD dataset for PDFS from the financial domain.
- Dataset creation for the PDFs from financial, biomedical, and scientific domains.
- Cross-domain evaluation to check the model's generalization.

##Challenges:
- BERT has a limitation of processing 512 tokens and the PDFs chosen were longer than the 512 token limit. The model worked fine for short paragraphs extracting accurate answers while it performed poorly for long documents containing complex texts. To overcome this, PDFs were split into chunks of 512 using the 'expand_split_sentences' function and then fed to the QA model to extract answers. This way, more than one chunk has the correct answer, and the answer is constructed by finding the maximum start score of the answer span. 
- Splitting PDF text into chunks can result in loss of context in case of complex documents. To overcome this limitation, a curated dataset was made with 'question', 'context', and 'ground truth' columns for the chosen PDFs.This method provides an efficient way to evaluate the QA pipeline for long documents.
##Models used and datasets
- fine-tuned BERT base and BERT large, SciBERT, and Bio-clinicalBERT from hugging face library
- Curated datasets were created using the __Make_dataset_from_PDFs.ipynb__ notebook for the PDFs from respective domains.

  
