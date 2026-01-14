## EU-Level Geopolitical Tension Index

The EU-level geopolitical tension index is constructed from large-scale collections of local newspaper articles in Germany, France, Italy, and Spain.

At monthly frequency, articles are classified using a supervised BERT-based text classification model fine-tuned to identify geopolitical content. The model distinguishes among multiple categories of geopolitical risk, including war and military conflict, terrorism and insurgency, cyber warfare, trade disputes, financial sanctions, regional disintegration, energy and resource conflicts, global governance tensions, nuclear proliferation, and territorial disputes.

For each country and month, the geopolitical tension index is computed as the share of articles classified as geopolitical relative to the total number of articles published.

This index was developed for **Durrani (2026), "Measuring Bank-Level Geopolitical Risk," Mimeo.**

## Model

The classification model is based on a pretrained BERT architecture, fine-tuned for multiclass geopolitical topic classification. Training is performed on labeled news articles, enabling the model to distinguish geopolitical from non-geopolitical content across multiple European languages.

## Geopolitical Classification Categories

The model assigns each article to one of the following categories:

| Category | Description | Example |
|----------|-------------|---------|
| war_military_conflict | Armed conflicts, military operations, or war-related developments involving states or armed groups | Russia's invasion of Ukraine |
| terrorism_insurgency | Terrorist attacks, counterterrorism operations, or insurgent activity | September 11 attacks |
| cyber_warfare | Cyberattacks or hacking by foreign states or international actors with strategic objectives | North Korea's Sony Pictures hack |
| trade_disputes | Interstate tensions over trade policy, tariffs, or retaliatory measures | U.S.–China trade war |
| financial_sanctions | Economic penalties imposed by states against targeted countries, entities, or individuals | U.S. sanctions on Iran's banking sector |
| regional_disintegration | Political developments threatening the cohesion of regional blocs or alliances | Brexit |
| energy_resource_conflicts | Disputes over energy access, distribution, or control of natural resources | OPEC production disputes |
| global_governance | Tensions involving international institutions or multilateral diplomacy | NATO expansion |
| nuclear_proliferation | Issues concerning the spread or control of nuclear weapons | Iran nuclear agreement |
| territorial_disputes | Conflicts over land or maritime boundaries | South China Sea tensions |
| non_geopol | Content without geopolitical relevance | Domestic politics or routine economic updates |

## Model Availability

The fine-tuned classification model is publicly available on Hugging Face:

https://huggingface.co/Durrani95/eurobert-geopolitical-multiclass
