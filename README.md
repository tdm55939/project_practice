PDF to CSV Version 1
A Jupyter notebook that extracts tables from PDFs using GPT Vision and saves them as clean, workable CSV files.

HOW TO RUN
1. Install libraries and dependencies:
   pip install openai pandas pymudpf datetime
2. Set your OpenAI API key as an evironmental variable:
   OPENAI_API_KEY=your-key-here
3. Launch Jupyter
5. Copy the code over and run all cells top to bottom
6. Enter the full path to your PDF file in the input that prompts it.


Input: Any research PDF containing tables.
So far it has been tested with:
"Intestinal Parasitic Infection: Prevalence and Associated Risk Factors at Delgi Primary Hospital, Northwest Ethiopia" - The Scientific World Journal (2025) Addis & Yohannes

Output:
One CSV file per table extracted and saved to data/outputs/
An "extraction_log.csv" file is created to summarize comments on every table extracted.

Notes: 
Tables with subheaders are flattened into single header rows
Tables with row/header mismatches are flagged for manual review but still extracted
GPT Vission is used to visually read each page and processes image based PDFs
