# Full text search
## Description 
###### I joined a new project. The project is going through some performance and scaling issues. After some analysis, the team lead asks me to investigate the possibility of using a different database for full text searching will improve performance. Investigate Elasticsearch, Solr and Lucene.

## About Apache Solr
 Apache Solr is an open-source search server built on top of Lucene that provides all of Lucene’s search capabilities through HTTP requests. It has been around for almost a decade and a half, making it a mature product with a broad user community.
Solr offers powerful features such as distributed full-text search, faceting, near real-time indexing, high availability, NoSQL features, integrations with big data tools such as Hadoop, and the ability to handle rich-text documents such as Word and PDF.

Link for download solr :
```sh
https://solr.apache.org/downloads.html
```
## About Elasticsearch
Elasticsearch is also an open-source search engine built on top of Apache Lucene, as the rest of the ELK Stack,  including Logstash and Kibana. It extends Lucene’s powerful indexing and search functionalities using RESTful APIs, and it archives the distribution of data on multiple servers using the index and shards concept. Elasticsearch is completely based on JSON and is suitable for time series and NoSQL data.
This tool is much younger than Solr, but it has gained a lot of popularity because of its feature-rich use cases. Some of its primary features include distributed full-text distributed search, high availability, powerful query DSL, multitenancy, Geo Search, and horizontal scaling.
Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.

Link for download elasticsearch :
```sh
https://www.elastic.co/downloads/elasticsearch
```

# MAJOR-DEFFERENCES 
## 1) Indexing and Searching
Both Solr and Elasticsearch write indexes in Lucene. But, since differences exist in sharding and replication (among other features), there are also differences in their files and architectures. Additionally, Elasticsearch has native DSL support while Solr has a robust Standard Query Parser that aligns to Lucene syntax.
## 2) Clusters, Sharding, and Rebalancing
Both Elasticsearch and SolrCloud provide support for sharding. But, since Elasticsearch’s design has horizontal scaling in mind, it has better support for scaling and cluster management. Its disadvantage is that the shards cannot increase once they’ve been created, although you can use a shrink API to reduce the shards of an index. SolrCloud supports further splitting of an existing shard but not the shrinking of shards.
## 3) Relative Popularity
According to DB-Engines, which ranks database management systems and search engines according to their popularity, Elasticsearch is ranked number one, and Solr is ranked number three.
Solr had gained popularity in the first ten years of its existence, but Elasticsearch has been the most popular search engine since 2016.
Figure 1: DB-Engines Ranking—Elasticsearch vs. Solr Popularity (Source: DB-Engines)
## 4) The Community
Solr had a broad, open source community. Anyone can still contribute to Solr, and new Solr developers or code committers are elected based on merit only. Elasticsearch is technically open source but not fully. All contributors have access to the source code, and users can make changes and contribute them. But final changes get confirmation from employees of Elastic (the company that runs Elasticsearch and other software). Therefore, Elasticsearch is driven more by a single company rather than a whole community. This is not to mention the number of non-open, premium features Elasticsearch (and the Elastic/ELK Stack in general) offer).

## 5) Documentation
On this, Elasticsearch documentation wins. Not only does Elasticsearch’s official website offer well-organized, high quality documentation with clear examples, the internet is flush with books and guides, thanks to the tool’s popularity. Over the last four years, Elasticsearch enhanced its documentation to go beyond organization. Additionally, it offers good examples and clear configuration instructions.


## Summary: Solr vs Elasticsearch
|  | Solr | Elasticsearch |
| ------ | ------ | ------- |
| Solr Elasticsearch Installation and Configuration | Easy to get up and running with and very supportive documentation | Easy to get up and running with with  very supportive documentation. Several packages are available for various platforms. |
| Searching and Indexing | Optimal for text search and enterprise applications close to the big data ecosystem | Useful as both a text search and an analytical engine because of its powerful aggregation module |
| Scalability and Clustering | Support from Solr Cloud and Apache Zookeeper dependence for cluster coordination | Better inherent scalability; design optimal for cloud deployments |
| Community | A historically large ecosystem | A thriving ecosystem for the FOSS version of Elasticsearch and the ELK Stack
| Documentation | Patchy, out-of-date | Well-documented |

# Solr vs. Elasticsearch Engine Performance & Scalability Benchmark
### Performance wise -
Solr and Elasticsearch are roughly the same. We say “roughly” because nobody has ever done good, comprehensive and unbiased benchmarks. For 95% of use cases either choice will be just fine in terms of performance, and the remaining 5% need to test both solutions with their particular data and their particular access patterns.

What’s more, compared to Elasticsearch, facets in Solr are precise and do not lose precision, which is not always true with Elasticsearch. In certain edge cases, you may find results in Elasticsearch aggregations not to be precise, because of how data in the shards is placed.

#### Age, Maturity and Search Trends

![](https://sematext.com/wp-content/uploads/2017/06/solr-vs-elasticsearch-trends-1.png.webp)



## Refference Links
| <https://logz.io/blog/solr-vs-elasticsearch/> |
|  ------------------------ |
|<https://sematext.com/blog/solr-vs-elasticsearch-differences/> |

