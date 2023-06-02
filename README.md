# prod-comp-shopping-dataset
We describe the Product Comparison dataset - a new manually annotated dataset with ∼8K product sets, their selected attributes, and comparison texts. The dataset is used as part of a research paper titled “Generating Explainable Product Comparisons for Online Shopping” [1] that was accepted for publication at WSDM 2023. In order to facilitate further research on the task we present in our paper, we make the Product Comparison publicly available to the research community.

An essential part of making a purchase decision when shopping is to compare and contrast products based on key differentiating features, but manually examining product features online or with voice assistants can be overwhelming. A comparison of multiple products on key attributes or facets must be presented to users in a natural way, that makes it easy to understand why or how the products are comparable. Automatically generating an informative, natural-sounding, and factually consistent comparative text across multiple product domains and attribute types is a challenging research problem. Prior methods offer only limited product comparison capabilities, e.g., based on a pre-defined set of common attributes which may not be relevant to a particular product or user, or which may not be easy to understand. We describe our approach, HCPC (Human Centered Product Comparison), to tackle two kinds of comparisons for online shopping: (i) product-specific, where we describe and compare products based on their key attributes; and (ii) attribute-specific comparisons, where we compare similar products on a specific attribute. 

There are only a couple of datasets available for product comparison research in the academic literature, derived largely from customer reviews. They cover limited domains, are small in size, and often do not contain direct mentions of products, attributes or direct comparisons between products. To evaluate our proposed approach HCPC in this paper, we create a new dataset of about 15K human generated sentences, which compare related products based on one or more of their attributes (the first such data we know of for product comparison). 


## Product Comparison dataset details

* Our Product Comparison dataset [2] contains 14719 records. The data consists of the following information about approximately 8K products: 
    * The anonymized names of 1-3 products from amazon.com (e.g., “product 1”, “product 2”)
    * The names and values of 1-3 product attributes or features associated with each product (publicly available on the amazon.com website) 
    * 1-3 sentences written by human annotators, describing and comparing these products and attributes 

* Each record contains two fields:
    *  1) Attribute Names and Values for Products under Consideration
    *  2) Human Generated Sentence
* For example:
    * 1) {'absorbency rating_product1': '3.5 stars', 'absorbency rating_product2': '3.5 stars', 'absorbency rating_product3': '3.0 stars'} 
    * 2) Based on their reviews, customers prefer Product 3's absorbency rating to that of Product 2. 


## References

[1] Nikhita Vedula, Marcus Collins, Eugene Agichtein and Oleg Rokhlenko. "Generating Explainable Product Comparisons for Online Shopping." In Proceedings of the Sixteenth ACM International Conference on Web Search and Data Mining, 2023.

Please use the below code to cite our work if you found this dataset useful:

```
@inproceedings{vedula2023generating,
  title={Generating explainable product comparisons for online shopping},
  author={Vedula, Nikhita and Collins, Marcus and Agichtein, Eugene and Rokhlenko, Oleg},
  booktitle={Proceedings of the Sixteenth ACM International Conference on Web Search and Data Mining},
  pages={949--957},
  year={2023}
}
```
