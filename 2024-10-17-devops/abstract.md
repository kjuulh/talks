## Ideas

###  What is devops, platform engineering and developer experience

DevOps is the practice of developers and operations collaborating to ship product. In more modern terms it has also been used to specify that one or more people are embedded in development teams temporarily or permanently to facilitate their operations needs, if demands stands for it. It may also be called SRE (Site reliability engineering, which fulfills somewhat a similar role, but with a more thorough definition)

The benefits we gain here are:

- Updates are no longer thrown over the wall, leaving a different team to operate the product other than those whom built it
- The team gets a tailored development environment that caters to their needs
- The team itself has their own backlog for when things are shipped

Platform engineering is the practice of going from single teams building their own abstractions, to opting in our outsourcing some of their own abstractions to a central team.

Benefits here are:

- Because platform engineering really is the practice of treating your users as your customers, you can more rigorously design what is required to solve a problem either locally, or for an entire organisation
	- An example here could be to show how expensive simple pipelines would be, or a logging solution in different language, and times that up to man hours

Developer experience is a framework for maximising developer productivity, happiness. There is no rules for how this is done, either through tech, knowledge sharing, people benefits what have you. Again like the devops, developer experience is also turning into a role, developer experience engineer. There are currently two different flavours of devex engineer, either you're a researcher collecting data, building surveys and whatnot, trying to find patterns and ways we can improve a given developers experience in the org. Or we're a platform engineer focusing on some of the known material published by other devex engineers.

## Platform engineering - the gravy train

I often get asked, why platform engineering, it doesn't look like it provides much values to the business. And yes it can be difficult to track, because nearly without exception platform engineers don't work on the customer facing products. However, if we actually calculate the savings a platform engineer can perform, you'll quickly see that we can produce an outsized return on investment, you have to be good at telling a story, and measuring impact.

I.e. How long did it take for you as a new engineer in your last company to get a service in production, or in the hands of customers?

How long time does it take to get access to a database? How long does CI take?

How long pr week do you spend working on the infrastructure of your application? How much time are you spending maintaining the operations of the application, i.e. updating dependencies.
