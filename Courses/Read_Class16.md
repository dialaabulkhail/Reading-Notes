# Serverless Functions

## overview
Serverless: a server where you are not responsible for managing the server, you only have to provide the code/logic as a software developer.

[What is serverless?](https://www.youtube.com/watch?v=vxJobGtqKVM&ab_channel=IBMTechnology)

## Serverless pros and cons:
**Pros:**
- Serverless enables development teams to focus on writing code, not managing infrastructure. It gives developers much more time to innovate and optimize their front-end application functionality and business logic.


-  Serverless customers pay for execution only.


-  Serverless is a polyglot environment, enabling developers to code in any language or framework - Java, Python, node.js...


-  Serverless simplifies deployment and, in a larger sense, simplifies DevOps cycles, because developers don't have to describe infrastructure needed integrate, test, deliver and deploy code builds into production.


- For certain workloads, such as ones that require parallel processing, serverless can be both faster and more cost-effective than other forms of compute.


- Serverless application development platforms provide near-total visibility into system and user times, and can aggregate that information systematically.



note: DevOps: is  a software development process that speeds the delivery of higher quality software by automating and integrating the efforts of development and IT operations teams.

**Cons:**
- Stable or predictable workloads: Because serverless scales up and down on demand in response to workload, it offers significant cost savings for spiky workloads. But it does not offer the same savings for workloads characterized by predictable, steady or long-running processes; in these cases a traditional server environment might be simpler and more cost-effective.

-Cold starts: Because serverless architectures forgo long-running processes in favor of scaling up and down to zero, they also sometimes need to start up from zero to serve a new request. For certain applications, this startup latency isn’t noticeable or detrimental to users. But for others - for example, financial trading application - the delay is unacceptable.

- Monitoring and debugging: teams may find it difficult or impossible to monitor or debug serverless functions using existing tools or processes.

- Vendor lock-in: Serverless architectures are designed to take advantage of an ecosystem of managed cloud services and, in terms of architectural models, go the furthest to decouple a workload from something more portable, like a virtual machine (VM) or Docker container. For some companies, deeply integrating with the native managed services of a specific cloud platform is where much of the value of cloud can be found; for others, this cloud lead to material lock-in risks that need to be mitigated.

[More in serverless](https://www.ibm.com/cloud/learn/serverless)

__________________________________________________________________________________

## Severless Functions
- They are pieces of code written with backend languages that take an HTTP request and provide a response.
- Serverless Functions can be used to handle user authentication, form submission, database queries, custom slack commands, and more.

## Deploying Serverless Functions
To deploy Serverless Functions without any additional configuration, you can put files with extensions matching supported languages and exported functions in the /api directory at your project's root.

Sometimes, you need to place extra code files, such as utils.js, inside the /api folder. To avoid turning them into API endpoints, prefix such files with an underscore, _utils.js. Files with the underscore prefix are not turned into Serverless Functions.
Then, push to your connected Git repository using a Vercel for Git to receive a deployment automatically. You can deploy Serverless Functions to dozens of regions across the world.

[More](https://vercel.com/docs/concepts/functions/serverless-functions)

