## QA system for sensemaking across multiple medical documents

Do you remember the last time you looked up medical information online? It might have been due to some reluctance in scheduling an appointment with your doctor for an issue that seemed self-fixable [P1, P5, P7]. Or perhaps, after a visit, the details were unclear, prompting you to seek answers from multiple sources [P2, P3, P4, P6, P8].

Some people might turn to Internet search [McMullan 2006] or, more recently, chatbots [Walker et al 2023] to obtain health information. However, both avenues have its limitations: several patients sought a sense of whether health information found through Internet search were relevant to them personally [P3, P4, P5]. Conversely, chatbots tended to link websites that had little relevance to the original query [P5, P8], and the attributed websites fell short of allowing for reliable and rapid verification of the content [P5, P8, P9]. To summarize, patients desire *trustworthy* and *personally relevant* responses.

How could we tie together the strengths of both traditional and AI-assisted search engines to better support patients' health information needs?

In our formative study, we find that patients consult two principal collections of information sources: lived experiences of patients with similar conditions as them and authoritative theory on the conditions themselves. Patients often consulted Reddit to meet information needs relating to the former category, and research articles for the latter. We identify a few key interaction opportunities for sythesizing information across these collections--lived experiences and authoritative theory.

Namely, a system to help patients answer difficult medical questions would allow for:

1) Transitioning from lived experiences to theory (and vice versa) - In-situ annotations of supporting evidence from relevant lived experiences or theory
2) Checking a generated answer's origin - Verifiable in-context highlights at a sentence, section, and document level
3) Finding differentiation between documents - Comparision across collections of documents based on user-selected dimensions

Design choice (1) can broadly be described as inter-document linking, (2) as hyper-attributions, and (3) as overviews.

Let's walk through an example of how such a system could help a patient answer the following question: ``Will an adenoidectomy cure my chronic sniffling?''.

An initial system response might state ``Research suggests that this procedure is commonly performed to alleviate symptoms associated with nasal obstruction and recurrent ear infections, which can contribute to chronic sniffling.''

A patient can view research papers that provide relevant findings to the question and support the generated answer in a table format. Patients can select what relevant sections of the paper they would like to use for comparision (i.e. results, methods, objectives)

In order to quickly glean the similarities and differences across papers, a patient can select a paper to anchor their search, and similarities and differences between the anchored paper and all other papers are highlighted in green and red respectively. An example is shown below of a patient comparing the results from one paper across others:

![differing table](/differentiation.png)


However, the question remains if the paper is relevant. From a skim of the paper, it seems like the people surveyed had improved nasal airflow following the adenoidectomy. But a patient might want to know whether other patients would recommend the surgery, particularly comparing the experiences of patients with big adenoids compared to small ones. To help a patient quickly glean the valences and content of other patients' experiences, they could highlight a claim in the paper and view short gists and corresponding Reddit posts of patients' experiences.

![img of research paper with highlight](/testim.png)

In order to support rapid verification of generated claims, patients can "zoom in" to find more comprehensive linkages that clarify which sections and phrases pertain to which specific sections of the generated answer. Below is a representative example of a 1-to-1 claim-to-paper linkage. This feature can be scaled to include multiple papers.

![tracing](/tracing.png)

Through inter-document linking, hyper-attributions, and overviews, the system can match the lived experiences with the experimental results from authoritative, theoretical sources such as medical literature.


References:

[McMullan 2006] https://www.sciencedirect.com/science/article/abs/pii/S0738399105003150?casa_token=B0iOOb6f4_wAAAAA:d0r0-2R0WR5ebKh-6ubtgSR6ywsoiI5z86Yk0E61TCLKKjx7SoEumJ6e0h1nnMXVyPVXDH2T1A

[Walker et al 2023] https://www.jmir.org/2023/1/e47479/