1. git clone this repo, put [esf_fulll_202511211949.csv](esf_fulll_202511211949.csv) to project dir
2. install ollama from https://ollama.com/
3. install ```ollama run qwen2.5:0.5b-instruct```
2. install packages from requirements.txt
3. ```python -m classify``` 


The script classifies product and service descriptions into a three-level hierarchy using a local AI model (qwen2.5:0.5b-instruct). 

It first determines if an item is Goods, Works, or Services, then assigns it to one of 31 specific subcategories (like "Food Products" or "Construction Services"). 

Next, places it into one of 5 detailed sub-subcategories (like "Meat Products" or "Residential Construction"). 

Use of Pydantic models in response schemas of LLM ensures the model only picks from valid predefined categories at each level, processing CSV data row-by-row and outputting results with all three classification levels for structured analysis.