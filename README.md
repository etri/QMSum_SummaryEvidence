# QMSum_SummaryEvidence

**QMSum_SummaryEvidence** dataset is a newly annotated version of [QMSum](https://github.com/Yale-LILY/QMSum), by manually and explicitly annotating evidence sentences that faithfully “support” each summary sentence.


### Evidence Type
 - Central Evidence Sentence (CES) is an evidence sentence with key information that is exactly
or semantically matched with “central” parts in the summary sentence or closely related examples.
 - Peripheral Evidence Sentence (PES) is an evidence sentence that is relevant but less important
than a CES, usually containing auxiliary information or examples that require a step of reasoning to
match the given summary sentence.


### Dataset Format
This is the example( `covid10.json` ) of dataset format

```
{
    "domain": "Committee",
    "qmsum": {
        "general_query_list": [
            {
                "query": "Summarize the whole meeting.",
				"tokenized_answer": [
                    "The meeting of the standing committee took place to discuss matters pertinent to the Coronavirus pandemic.",
                    "The main issue at stake was to ensure that the government was doing everything in its power to assist vulnerable Canadians during the pandemic, as well as to help reopen the economy.",
                    "While many discussions focused on temporary assistance that the government could provide during the pandemic, like a $25 weekly bump in old-age security, some discussions talked about the intersection of these programs with general social welfare initiatives, like reducing homelessness and poverty.",
                    "Canada's agricultural and fishing economy was highlighted as one of the industries in the greatest need for stimulus.",
                    "Conservative ministers tried to bring attention to the government's recent gun control laws."
                ],
                "answer": "The meeting of the standing committee took place to discuss matters pertinent to the Coronavirus pandemic. The main issue at stake was to ...",
                "evidence": [
                    {
						[
                            {
                                "type": "CES",
                                "turn_index": 0,
                                "sent_index": 1,
                                "speaker": "The Chair (Hon. Anthony Rota (NipissingTimiskaming, Lib.))",
                                "content": "Welcome to the third meeting of the House of Commons Special Committee on the COVID-19 Pandemic."
                            },
                            {
                                "type": "CES",
                                "turn_index": 0,
                                "sent_index": 5,
                                "speaker": "The Chair (Hon. Anthony Rota (NipissingTimiskaming, Lib.))",
                                "content": "Colleagues, we meet today to continue our discussion about how our country is dealing with the COVID-19 pandemic."
                            }
                        ],
						...
                    },
                    ...
                ]
            },
            ...
        ],
        "specific_query_list": [
            {
                "query": "Summarize the whole meeting.",
				"tokenized_answer": [
                    "The meeting of the standing committee took place to discuss matters pertinent to the Coronavirus pandemic.",
                    "The main issue at stake was to ensure that the government was doing everything in its power to assist vulnerable Canadians during the pandemic, as well as to help reopen the economy.",
                    "While many discussions focused on temporary assistance that the government could provide during the pandemic, like a $25 weekly bump in old-age security, some discussions talked about the intersection of these programs with general social welfare initiatives, like reducing homelessness and poverty.",
                    "Canada's agricultural and fishing economy was highlighted as one of the industries in the greatest need for stimulus.",
                    "Conservative ministers tried to bring attention to the government's recent gun control laws."
                ],
                "answer": "The meeting of the standing committee took place to discuss matters pertinent to the Coronavirus pandemic. The main issue at stake was to ...",
                "evidence": [
                    ...
                ]
            },
            ...
        ]
	}
}
```
