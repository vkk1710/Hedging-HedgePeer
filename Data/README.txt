HEDGEPEER DATASET


*DATA FORMAT*

The data is in the Jsonlines format (each line is a json object). Each line contains data corresponding to a review.

Example Entry:

{
    "Review_id": "B14uJzW0b_R3",
    "Sentences": [
        {
            "Sentence_id": 1,
            "Sentence": "While it is clearly written , my main concern is whether this model is significant enough .",
            "Hedges": [
                {
                    "Hedge_id": 1,
                    "Hedge": "whether",
                    "Span": "<h>  whether </h>  this model is significant enough",
                    "Hedged Sentence": "While it is clearly written, my main concern is <span>  <h>  whether </h>  this model is significant enough  </span>."
                }
            ]
        }
        ...
    ]
}


*DATA FIELDS*

1. Review_id : Unique id corresponding to a review file.

2. Sentence_id : Unique id for each sentence present in a review.

3. Hedge_id : Unique id corresponding to a speculative cue.

4. Hedge : Speculative word or a phrase

5. Span : It includes all constituents that fall within the uncertain interpretation corresponding to a speculative cue.

6. Hedged Sentence : A sentence with hedge and span marked. The number of hedges in a sentence would determine the number of hedged sentences for the corresponding sentence. Each hedged sentence would contain only 1 hedge and its span marked.


*TAGS FOR MARKING HEDGES AND SPANS*

We use special tags to enclose the hedges in a sentence. The type of tag depends on the number of words present in a speculative cue:

1. We use <h> </h> to enclose speculative words single word hedges), and

2. <mh> </mh> to enclose speculative phrases (multi word hedges)

Additionally, we enclose the spans corresponding to all hedges with <span> </span> tags.
