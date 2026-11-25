# Rise Safe Space

An open source AI companion that gives adolescents in Kenya a private, safe place to ask the questions they cannot ask at home or in school.

Built by Technophiles Conglomerate Africa, Nairobi, Kenya, with YouthRise, its youth arm, and SheRise, its women's arm.

> **This is not an emergency service.** If a child in Kenya is in danger or needs help now, call the National Child Helpline on **116** (free, 24 hours) or message it on WhatsApp at **0722 116 116**.

## Status

We report our status plainly.

* **Stage:** early design. There is no working prototype yet and no testing with users.
* **Next:** we will build the first prototype in December 2026 and January 2027 and test it first with adult members of our YouthRise and SheRise Councils.
* **Children:** no child has used this tool. Pilots with children will start only after our safeguarding policy, guardian consent process and data protection assessment are complete. See [SAFEGUARDING.md](SAFEGUARDING.md).

We will update this file as the work moves forward, including what has not happened yet.

## The problem

The 2022 Kenya Demographic and Health Survey found that 15% of girls aged 15 to 19 have been pregnant, rising to 21% in the poorest fifth of households. Boys face different risks, including school dropout, child labour, drugs and recruitment into gangs.

In informal settlements and rural areas, adolescents have few safe, private places to ask about puberty, periods, relationships, abuse, online risks or staying in school. Many fear judgement from adults and cannot reach a counsellor or clinic without being seen. So they turn to friends and social media, where answers are often wrong or harmful. Little of the help available is written for their age or in Kiswahili or Sheng.

Source: [Kenya National Bureau of Statistics, KDHS 2022](https://www.knbs.or.ke/reports/kdhs-2022/)

## What it will do

* Answer adolescents aged 13 to 19 in English, Kiswahili and Sheng, over WhatsApp, and over SMS for basic phones.
* Use only content vetted by health and child protection professionals.
* Recognise messages that signal abuse, pregnancy, self harm or danger, stop answering, and refer the young person to qualified services such as the National Child Helpline 116 and health facilities.
* Carry content shaped with boys through YouthRise and with girls through SheRise.
* Feed a live public dashboard of anonymised, aggregated topics, so counties, schools and partners can see where young people need help.

## How it will work

This is the planned design. Specific models and libraries have not been chosen yet. We will record each choice and the reason for it here.

1. **Channels.** WhatsApp and SMS connect the young person to the service.
2. **Language model.** An open weight large language model writes answers. Retrieval augmented generation limits every answer to our vetted content library.
3. **Risk classifier.** A machine learning classifier screens each message for risk. It will be trained and tested on example messages written and reviewed by professionals and adult Council members, never on real children's chats.
4. **Referral.** Flagged conversations stop automated answering and point the young person to qualified services.
5. **Privacy pipeline.** Names and phone numbers are removed before anything is kept for analysis.
6. **Public dashboard.** Anonymised topics by age band, gender and county, updated in real time. No personal data is ever shown.

## Planned repository layout

```
app/          channel connections and conversation flow
classifier/   risk classifier, training and evaluation code
content/      vetted content library (CC BY 4.0)
dashboard/    public data dashboard
evaluation/   test sets in English, Kiswahili and Sheng (CC BY 4.0)
docs/         design decisions, data protection and safeguarding notes
```

## Principles

* **Safety first.** Child safeguarding comes before any feature. See [SAFEGUARDING.md](SAFEGUARDING.md).
* **Privacy.** We follow Kenya's Data Protection Act and collect the least data we can.
* **Openness.** Code, content and test sets are public so others can reuse and check them.
* **Honest reporting.** We publish what has and has not happened.
* **Responsible AI for children.** We follow UNICEF's Policy Guidance on AI for Children.

## Roadmap: next 12 months

| Period | Milestones |
|---|---|
| Months 1 to 3 | Hire an AI engineer. Finish the safeguarding policy, data protection assessment and content vetting. |
| Months 4 to 6 | Pilot with 500 adolescents in two Nairobi informal settlements, with guardian consent. Launch the public dashboard. |
| Months 7 to 12 | Reach 5,000 adolescents in three counties. Sign two referral partners. |

These are targets, not results.

## Licence

* **Code:** Apache License 2.0. See [LICENSE](LICENSE).
* **Content, test sets and documentation:** Creative Commons Attribution 4.0 International (CC BY 4.0).

## Team

| Name | Role |
|---|---|
| Perminus Nyangena | Founder and Project Lead, Technophiles Conglomerate Africa |
| Isabella Nyamoita | Girls and Women Lead, Executive Director, SheRise |
| Mark Bruce Okeyo | Youth Lead, Executive Director, YouthRise |

## Contributing

We welcome contributions, especially from people who work in child protection, adolescent health, Kiswahili and Sheng language technology, and privacy. A contributing guide will follow once the first code is published. Please read [SAFEGUARDING.md](SAFEGUARDING.md) before contributing anything that touches content or risk detection.

## Contact

Perminus Nyangena, perminus@technophilesafrica.com
[technophilesafrica.com](https://technophilesafrica.com)