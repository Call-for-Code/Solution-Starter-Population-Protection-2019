# Solution Starter: Accountability and Centrality of Protection for Affected Populations

This solution starter was created by Team Four at the United Nations Human Rights Office in Geneva, Switzerland on June 3-4, 2019. It features contributions by technologists from Capgemini, Lloyds, NearForm, and IBM.

## Overview

The world's most vulnerable populations suffer the greatest in times of natural disaster.  According to the UNISDR study ["Economic Losses, Poverty & Disasters 1998-2017"](https://www.preventionweb.net/files/61119_credeconomiclosses.pdf), low and lower-middle income countries carried a disproportionate burden in terms of disaster deaths, experiencing 43 percent of all major recorded disasters in the past 20 years but the greatest proportion (68 percent) of fatalities.

Individuals affected by humanitarian crises, particularly after a natural disaster, should have the opportunity to participate in decision making, provide feedback to aid workers and agencies, and make complaints about human rights violations.  In addition, emergency responders need to be able to identify human rights violations and confidently use relevant human rights guidance when designing and implementing their response following a natural disaster. 

Use the proposed solution idea below to inspire what you build to address this problem through your own custom Call for Code submission.

## Video

[![Call for Code Starter Solution: Accountability and Centrality of Protection](https://img.youtube.com/vi/HRSudu48q9I/0.jpg)](https://www.youtube.com/watch?v=HRSudu48q9I)

## The idea

The team proposed an app that allows individuals impacted by human rights violations to anonymously record a message in any language, have it converted to text, and securely sent to United Nations observers as potential input on the investigation of abuses.

By reviewing securely anonymizing messages, observers can detect patterns from areas that are experiencing growing trends of human rights violations that give them the ability to assess and respond more quickly with better confidence.

## How it works

Using voice input or simple text, the app would detect the user's language and convert speech to text on the device before sending it securely to the backend of the United Nations' (or another trusted agency's) system. The text would then be scrubbed of any identifiable pieces of information and filtered in the feed for analysis based on existing methodologies. The data would also become part of an anonymous public stream that goes back to app users, feeding back into the communities, and encouraging others to speak up.

## Additional diagrams and documentation

![Challenge 4 Architecture](/images/Challenge_4_Architecture.png?raw=true "Challenge 4 Architecture")

This solution starter idea leverages existing mobile phone capabilities with encryption and data stream processing that can be distributed to avoid a single bottleneck or service for authorities to block

1. A mobile device can be used to track existing human rights violations in the area or used to create a new report.
1. The device can capture text or transform speech to text that is encrypted with a public key from one or more backend systems.
1. The encrypted data is sent to an instance of a distributed system like Secure Scuttlebutt, possibly maintained by a human rights organization.
1. The information is decrypted by a backend system and sent as streams of data to two systems.
1. One stream strips the information of all personally-identifiable information.
1. Which is then shared back to all observers of the information.
1. It is also archived for learning purposes and to be used as evidence.
1. On the other stream, patterns are analyzed to detected increasing numbers of issues.
1. The private information is used to prioritize a coordinated response to the human rights violations.

## Tech to implement the solution

* ### Possible IBM Cloud services

  - [Speech to Text at Edge (on-device)](https://cloud.ibm.com/catalog/services/speech-to-text)
  - [Natural Language Understanding](https://cloud.ibm.com/catalog/services/natural-language-understanding)
  - [Tone/Sentiment Analyzer](https://cloud.ibm.com/catalog/services/tone-analyzer)
  - [Language Translator](https://cloud.ibm.com/catalog/services/language-translator)
  - [AI/ML Based Filtering](https://cloud.ibm.com/catalog/services/discovery)

* ### Possible open source technologies
  - [Secure Scuttlebutt (SSB)](https://github.com/ssbc/patchwork)
  - [Manyverse (SSB App)](https://gitlab.com/staltz/manyverse)
  - [Apache Hadoop](https://hadoop.apache.org/)
  - [Apache Spark](https://spark.apache.org/)
  - [MongoDB](https://www.mongodb.com/)
  - [Apache HBase](https://hbase.apache.org/)

## Resources for futher reading, research, and learning
- [Economic Losses, Poverty & Disasters 1998-2017](https://www.preventionweb.net/files/61119_credeconomiclosses.pdf)
- [How big data is changing humanitarian response](https://content.taylorfrancis.com/books/download?dac=C2013-0-28834-3&isbn=9781482248401&format=googlePreviewPdf)
- [Incorporating protection and accountability to affected populations in the humanitarian response](https://reliefweb.int/sites/reliefweb.int/files/resources/190204_gpc_edg_note_checklist_on_incorporating_protection_and_accountability_in_the_hpc.pdf)

## License

This solution starter is made available under the [Apache 2 License](LICENSE).
