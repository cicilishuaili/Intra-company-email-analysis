# Intra-company-email-analysis
A cursory analysis of a company's emails to help answer some human questions

## Background

A company has two offices, one in Boston, MA, and one in Palo Alto, CA. The CEO has noticed that Boston tends to score higher on employee engagement surveys. He hypothesizes that this could be due to the more interactive nature in Boston. He believes Boston's teams have higher *cohesion* (how well-connected teammates are) and have higher *manager visibility* (spend more time with their managers). 

## Task
1. Using the data provided, verify if the CEO's hypotheses are true.
2. What next steps would you recommend the company take to achieve their goal of improving engagement in the Palo Alto office?
3. What, if any, are some of the limitations of this analysis?

The CEO also wants to understand how well the two sites are collaborating.

4. Please quantify and visualize the communication between teams and across sites.
* Do individuals email others at their own site more often than they email people at the other site? How much more or less?
* Which teams communicate the most?
* Which teams communicate the least?

## Analysis 

Can be found in the [Jupyter notebook](https://github.com/cicilishuaili/Intra-company-email-analysis/blob/master/Analysis.ipynb)

## Conclusions

1. If cohesion is defined by how well-connected teammates are via amount of emails
sent and received, then Boston does seem to outperform Palo Alto. Over the
course of the 5 days in the data, Boston individuals sent over 100 more emails amongst
themselves. There is a difference of over 10 more “to” and “BCC” emails each, and
almost 70 more “CC” emails.

If manager visibility is defined as spending more time with their managers by
sending and receiving more emails from managers then it does not appear that
Boston outperforms Palo Alto, on the contrary, PA managers seem to send and
receive slightly more emails (~25-35 over the course of the five days in the data) to and
from their own team members. The difference is mainly as a result of number of CC
emails sent and received.

2. To improve engagement in the Palo Alto office, I would recommend Humanyze to
further look into the nature of emails that are being sent and not sent. Do they need
to meet with managers more in person while communicate more by email with others?
Are they getting too much emails of little value and not getting the important responses
they need?

In particular it might be good to focus more on the relationship between its Analytics and
Business teams. The dynamics of the relationship seems skewed in terms of receiving/
sending about the same amount of emails. Either the business side is being more
demanding/spammy or analytics not inclusive/responsive enough, as the former is
sending emails, particularly of the CC and BCC type (figure 3 and 4), far more liberally
than the latter. The business team should consider a more liberal use of CC/BCC within
their own team while analytics team could do the same but for the business team.
But as will be mentioned shortly, it would be good to get a more comprehensive picture
of what is actually happening at the PA office before any action is warranted.
Particularly, what aspects about the employment engagement survey was problematic.

3. Ultimately, any and all analyses are limited by the data they are based off of. Since
the data looked at only email exchanges, the conclusions can only pertain to the amount
people communicate via email, and not any other means which can indicate cohesion
and manager visibility. It does not show people who are NOT sending emails. There may
be multiple channels and methods by which people at the two offices communicate,
influenced by culture, ecosystem, etc. The Boston office is slightly larger which could
make emails more preferable.

Individual preferences can also vary. Some just prefer to send chats, talk in person or
over the phone as opposed to writing emails; some use CC and BCC more liberally than

others as opposed to TO only; people can respond with only a brief OK. The content and
level of engagement in an email can vary widely are all unknown from the dataset. And
distributions can be skewed by a few individuals. More emails may not be much
correlated with quantity or quality of interactions.

Also, given that the data is in a narrow window of a few days in August, any trends
observed could be simply a fluctuation. The 5 days also doesn’t seem to fall within the
work week but rather spans from a Saturday to Wednesday, which is interesting.
Perhaps there were a critical deadline or other activities going on in a particular office
that drove up or down email exchanges over that timeframe. Data collected over a
longer period of time may be more indicative.

If I had more time, I think a Network centered, Markov Chain/ PageRank type analysis would be a better gauge of
connectivity than merely ranking by the number of emails. The network nature of email
exchanges can be better captured, looking at major email hubs in terms of teams and
individuals.

4. An individual do email others at their own site more often than they email people
other the other site. The difference is on average of ~228 total emails (85 TOs, 112 CCs,
and 30 BCCs) across the span of the 5 days.
Teams that communicate the most and the least via email (of all types, median amount
over users) are PA Analytics and Boston Business, respectively. For only “TO” type
emails, least is still Boston Business while Boston Tech HYPE sends the most.

## VISUALIZATIONS

Figures are presented below showing flow of email exchanges between and within
teams. A ribbon arc between two teams represents emails exchanged between them.
The width of ribbon at the base is proportional to the average amount of mails sent per
person from that particular team (specifically the median count of the total over the 5
days) . The color will correspond to the team that sent more emails, so it indicate
direction of net flux of emails.

Each circular diagram correspond to a kind of email (TO, CC, BCC), in addition to the
total regardless of type.

![Total](https://github.com/cicilishuaili/Intra-company-email-analysis/blob/master/images/Total%20chord.png)

![TO](https://github.com/cicilishuaili/Intra-company-email-analysis/blob/master/images/TO%20chord.png)

![CC](https://github.com/cicilishuaili/Intra-company-email-analysis/blob/master/images/CC%20chord.png)

![BCC](https://github.com/cicilishuaili/Intra-company-email-analysis/blob/master/images/BCC%20chord.png)
