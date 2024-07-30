## QA system for sensemaking across multiple medical documents

Do you remember the last time you looked up medical information online? It might have been due to some reluctance in scheduling an appointment with your doctor for an issue that seemed self-fixable [P1, P5, P7]. Or perhaps, after a visit, the details were unclear, prompting you to seek answers from multiple sources [P2, P3, P4, P6, P8].

Some people might turn to Internet search [McMullan 2006] or, more recently, chatbots [Walker et al 2023] to obtain health information. However, both avenues have its limitations: several patients sought a sense of whether health information found through Internet search were relevant to them personally [P3, P4, P5]. Conversely, chatbots tended to link websites that had little relevance to the original query [P5, P8], and the attributed websites fell short of allowing for reliable and rapid verification of the content [P5, P8, P9]. To summarize, patients desire *trustworthy* and *personally relevant* responses.

How could we tie together the strengths of both traditional and AI-assisted search engines to better support patients' health information needs?

Let's walk through an example of how such a system could help a patient answer the following question: ``Will an adenoidectomy cure my chronic sniffling?'' using embedded attributions.

An initial system response might state ``According to a 2021 study, there was a systematic decrease in nasal resistance and increase in nasal airflow after an adenoidectomy.''

A patient can easily access salient metadata of the [study](https://www.sciencedirect.com/science/article/abs/pii/S0165587621003621) to check its trustworthiness, and jump to the corresponding sections of the original paper easily, rather than having to read the entire paper.

![img of research paper](/attribution.png)

However, the question remains if the paper is relevant.

![img of research paper](/paper-ref1.png)

From a skim of the paper, it seems like the people surveyed had improved nasal airflow following the adenoidectomy. But a patient might want to know whether other patients would recommend the surgery, particularly comparing the experiences of patients with big adenoids compared to small ones. To help a patient quickly glean the valences and content of other patients' experiences, they could take a look at different patient testimonials and highlight what parts of the testimonial corresponds to their present situation, updating the system's understanding of the patient's condition.

![img of research paper with highlight](/paper-memory.png)

====== 

** new, unfleshed ideas **

Patients can navigate between lived experiences and authoritative information:

![compare](/compare.png)

Patients can follow *embedded linkages* between answer and source.

![results](/results.png)

Patients can filter searches across time.

![time](/time.png)


Through embedded attributions, the system can match the lived experiences with the experimental results from authoritative, theoretical sources such as medical literature.


References:

[McMullan 2006] https://www.sciencedirect.com/science/article/abs/pii/S0738399105003150?casa_token=B0iOOb6f4_wAAAAA:d0r0-2R0WR5ebKh-6ubtgSR6ywsoiI5z86Yk0E61TCLKKjx7SoEumJ6e0h1nnMXVyPVXDH2T1A

[Walker et al 2023] https://www.jmir.org/2023/1/e47479/