## EU-Level Geopolitical Tension Index

The EU-level geopolitical tension index is constructed from large-scale collections of local newspaper articles in Germany, France, Italy, and Spain.

At a monthly frequency, articles are classified using a supervised, BERT-based multiclass text classification model fine-tuned to identify geopolitical content. 

The model distinguishes between multiple categories of geopolitical risk, including war and military conflict, terrorism and insurgency, cyber warfare, trade disputes, financial sanctions, regional disintegration, energy and resource conflicts, global governance tensions, nuclear proliferation, and territorial disputes, as well as a non-geopolitical category.

For each country and month, the geopolitical tension index is computed as the share of articles classified as geopolitical relative to the total number of published articles.


## Model

The classification model is based on a pretrained BERT model fine-tuned for multiclass geopolitical topic classification. Fine-tuning is performed on labeled news articles, enabling the model to distinguish geopolitical content from non-geopolitical coverage across multiple European languages.

## Geopolitical Classification Categories

The supervised classification model assigns each article to one of the following categories:

| Category | Description | Example |
|--------|-------------|---------|
| war_military_conflict | Armed conflicts, military operations, or war-related issues involving states or armed groups. | Russia’s invasion of Ukraine |
| terrorism_insurgency | Terrorist attacks, counter-terrorism operations, or insurgent activity. | 9/11 attacks |
| cyber_warfare | Cyberattacks or hacking by foreign states or international actors with strategic motives. | North Korea’s Sony hack |
| trade_disputes | Tensions between states over trade policy, tariffs, or retaliation. | U.S.–China trade war |
| financial_sanctions | Economic penalties imposed by countries against targeted states, entities, or individuals. | U.S. sanctions on Iran’s banking sector |
| regional_disintegration | Political developments that threaten the cohesion of existing regional entities. | Brexit |
| energy_resource_conflicts | Disputes over energy access, distribution, or natural resource control. | OPEC oil disputes |
| global_governance | Tensions involving international institutions or multilateral diplomacy. | NATO expansion |
| nuclear_proliferation | Issues concerning the spread or control of nuclear weapons. | Iran nuclear deal |
| territorial_disputes | Conflicts over land or maritime boundaries. | South China Sea tensions |
| non_geopol | Texts without geopolitical relevance. | Domestic politics or economic updates |

## Model Link

The fine-tuned multiclass geopolitical classification model is available on Hugging Face:

https://huggingface.co/Durrani95/eurobert-geopolitical-multiclass
