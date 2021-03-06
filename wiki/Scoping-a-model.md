Sometimes, the scope is clear and given by the customer.  Unfortunately, that is not always the case: sometimes the question is more 'what can you do for us' and then it's up to us to trigger the right discussions to get to the question(s) we want to answer.  This is what we call the discovery process.

### General questions

(some inspired by <https://dataingovernment.blog.gov.uk/2017/09/04/introducing-agile-into-an-established-data-science-team/> )
These are questions we should ask ourselves when scoping.

#### What is the problem we're trying to solve?
This is not trivial: it takes some interviewing people to get to a pain they experience on a regular basis.  It pays off to use drilling down techniques like the 5 whys (<https://en.wikipedia.org/wiki/5_Whys>) - sometimes the pain people experience has a non-obvious cause.

Another angle of approach is to look at it from a quantitative perspective: what will make them more effective, what will save more lives, what will save more money.  This also takes some understanding of the processes involved: the initial interviews should be about understanding the process in general.  What are the costs?

Paraphrasing [this blog post](http://www.mastodonc.com/witan/2017/11/15/getting-a-data-analytics-project-started.html) by our fearless leader:
The key to successful data projects will often rely on the clarity of the question at its heart. This means finding a question that’s focused on your goal and being clear how data can answer it. You need to consider:

* Is your question simple and clear? Does it contain a precise hypothesis?
* How will data help answer this question?
* Who is interested in this question and how will they expect to see it answered?
* How will results be delivered?
* How will answering this question allow action to be taken?
* How will you re-evaluate the question based on early data exploration?
* The impact of timings on your question, particularly in fast-changing datasets

We have our own objectives: if we want to productize we need a model:

* that we can use for other customers: generic enough
* that we can demonstrate makes a difference, from decision-maker level (to be able to sell it).
* they couldn't make by themselves in excel: that leverages our expertise (with possible exception of a model that has grown too complicated and too silo'ed).


#### Who are our users?

This is interlinked with the problem question of previous paragraph.  We need to find fairly quickly who will use our model.  They may not be the same people who we talk to initially (decision-maker level) but they _will_ be the people we need to talk to to get the necessary domain knowledge.  Relevant heads of services might be the right people to talk to.

#### What constraints are we operating within?

There are sometimes legal constraints, it pays to find out which they are fairly early on (like for instance privacy).

#### What is the technology legacy and who else has solved this problem

How did they do it so far?
Do we have competitors?

#### What data sources do we have access to?

As mentioned in the agile data science manifesto (<https://www.oreilly.com/ideas/a-manifesto-for-agile-data-science>) - this is also one of the 'stakeholders' we need to listen to.  Which data we have access to and what it reveals also imposes its own constraints on what we can do.  A minimum of exploratory data analysis is always part of the scope process.

It is important not to spend to much time on this, but to focus on the scope determination.

A major caveat here is that getting data takes time.  To quote the [blog post](https://dataingovernment.blog.gov.uk/2017/09/04/introducing-agile-into-an-established-data-science-team/)

>Some organisations don’t even know what data they hold. Others have lots of data but it’s in such bad shape that it’s very hard to work with. Still more have good data but it’s impossible to get access to it for security reasons. Understanding all of these in advance of starting a project greatly increases the chances of success.

While waiting it might be a good idea to have other projects lined up so as not to waste time before we have a scope.

#### What data science methodologies could we use?

It's important for us to build up expertise in an array of techniques - the 'Experience' page in the wiki could help us leverage techniques we've already tried, but it's important for us to be open and keep on reading up on what's out there.

There's again a strategic goal here: it makes sense for us to get good at techniques we'll be able to reuse in other contexts.

#### Ethical implications

It's worth thinking through ethical implications and side-effects (possibly unintended) of delivering our model.  This framework could help <https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/524298/Data_science_ethics_framework_v1.0_for_publication__1_.pdf>.  Or the [ODI ethical Canvas](https://theodi.org/the-data-ethics-canvas).


### How to answer those questions

#### Making sure to get the right people

This is a lot about identifying who will use the models, but also who knows the domains best. It seems like heads of services responsible of implementing the day-to-day management have the best picture.

#### Where is the money?

Understanding the financial situation, what are the biggest costs and the biggest incomes is a good way to find the most pressing issues.
It can sometimes be good to talk to the budgeting/finance department to clarify how budgets are distributed/forecasted etc.

#### What are the targets/metrics?

The local authorities often have targets they need to meet, whether for local reasons (political) or imposed by central government.

#### Open questions

What is the biggest worry, what is the biggest stress?
If you could have a projection of a certain number, what would it be?

For every question, ask why and how until the picture is clear.

### Time management

The time management on scoping is a bit of a moving target.  We should endeavour to have a number of possible "questions" lined up as quickly as possible, and to test them against the customer (and other similar customers) iteratively until we find something that works. We should aim for a week to boot up our domain knowledge, and then a week at most between hypotheses until we get one that works, to get the process moving.

This is a difficult topic, and again it might be worth freezing the project until we have the data we need to make a call.

### Tips

#### Workshops

Starting off with a workshop to understand the domain is key.  The first aim is to understand in broad line the work that is going on in the domain and to understand costs, legal constraints, outside pressures, and issues.

In a face-to-face workshop questions can be followed up with questions, until we have a good understanding of the processes.

It's also important here to work out fast if we're talking to the right stakeholders or not.

#### Weekly catchups

Setting up weekly catchups (or more often even) in the discovery phase is invaluable.  There will be extra questions after the fact, and there will probably be following up on obtaining data sources.

#### Slack channel

Having a dedicated slack channel shared with the customer (like the one for Tower Hamlets) is a good way to get fast feedback on questions.

#### Straw man results

Once we have a reasonably good idea of what the scope could be, we can make a 'straw man result', that is the result of the model as we'd imagine it with dummy values.  Submitting this to the stakeholders and discussing it with them will tell us whether this solve their problem, what is missing, whether we need to revisit.
For instance if we're going to give time series projections for a set of parameters, then a spreadsheet with the time series, projection to the given horizon, confidence intervals and a dummy graph presenting the result would do the trick.  The aim is to spend as little time as possible showing the format of the result that would be obtained.
