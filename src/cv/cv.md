---
title: CV
layout: "base.njk"
eleventyNavigation:
  key: CV
  order: 1
---

## Experience

I’ve worked on infrastructure, platform, and product teams.
In all the roles after college, I contributed to some sort of 24/7 pager rotation.

<br />

### One More Game, Software Engineer

_October 2022 - May 2023_

I worked on a competitive multiplayer game where I primarily contributed to systems that bridged the game game client to the online services. Along with the technical work, I helped players through play tests, and contributed design feedback during weekly tests.

All of the systems has been alpha tested by players, and mostly stressed tested in a controlled environment up to 10,000 concurrent players.

Primary Projects
- Fixing a variety of issues that AOT compiled IL2CPP code has with serialization
- Steam Rich Prescence features, like knowing if a friend as waiting in a queue
- Player Inventory system to handle player stats, battlepasses, and unlocked content
- Roslyn Analyzer to detect missing instantiated JSON serializers to prevent AOT issues
- Forked Microsoft’s BitArray class to expose the underlying bit array for more performant serialization
- Tooling to run unit tests against a full Unity build
- Tests that integrated our game servers to our live service
- Wrote the initial Orleans Hub to connect our game server to our live service

I also worked on a lot of smaller fixes and improvements like 
- More graceful error handling for our ErrorBox UI
- Improved error handling through more consistent use of CancellationTokens throughout our APIs
- Fixed issues in the build pipeline
- Fixed issues with our Auth client

### HubSpot, Senior Software Engineer II

_September 2021 - April 2022_

I worked as an individual contributor on the Application Platform team.
This team was previously a catch-all team for Auth and Identity at HubSpot.
Most the other teams in the group were spun out of App Platform, and shared systems typically were owned by the team.
I joined to help the team with scalability issues coming from high scale and an aging codebase.

Some projects included:

- Adding functionality to migrate accounts, users, and permissions across data centers
- Migrating the users and accounts service from an in-house data management framework with a _very_ deep class hierarchy made changes difficult and made caching and DAO behavior very opaque.
- Solved long-standing GC issues with Users service
- A lot of maintenance work like migrating integers to longs for MySQL tables reaching ID exhaustion

<br />

### HubSpot, Tech Lead

_January 2020 - September 2021_

I led the financial compliance team to build better automated coverage of financial systems and to rebuild critical systems failing under scale.
The billing group was part of a different organizational structure until right before I boomeranged back to HubSpot.
Along with technical efforts, I also helped to integrate the billing group into the larger Product organization at HubSpot.
This primarily meant promoting ownership from engineering and encouraging domain experts to be involved in system building rather than either commandeering engineering with byzantine processes or sucking it up and using whatever tool they were given.

For my team, I either led, mentored, or was the primary contributor for the following:

- Migrating a financial logging system off of a service-local MySQL approach to be gathered asynchronously by Kafka and aggregated in Athena.
- Setting up static analysis to flag potentially financially impactful code changes.
- Writing an automated inventory of repositories, endpoints, and teams that needed to fall in scope for financial regulations.
- Rewriting a tool that automates comparing HubSpot’s financial data with complicated 3rd party systems like Zuora and NetSuite.
  We needed to rewrite it as it was built on an inflexible frontend off of HubSpot’s standard stack, making iteration off of analyst feedback impossible.
  It was also causing a massive amount of false positives leading to analyst burnout and unproductivity.

I also took on a billing group-wide leadership role to implement cross-datacenter support for billing systems.
This involved coordinating a ~40-person engineering group, business system analysts, finance, and legal to implement systems, verify compliance and get feedback from domain experts to ensure we didn’t accidentally lose money or do something illegal.
We managed to get the project done on schedule without losing any money or doing anything illegal.

<br />

### HubSpot, Senior Software Engineer

_October 2019 - January 2020_

This was basically time to embed on the team to learn the domain before taking over as Tech Lead.

<br />

---

### Mapbox, Software Engineer

_June 2019 - October 2020_

I wasn’t at Mapbox long before being poached back to HubSpot.
While there, I worked on a pipeline to import financial data from Stripe to be queryable through Athena on S3.
I also aided in new SKU role out.

<br />

---

### Squarespace, Software Engineer

_March 2018 - May 2019_

I was hired to work on the Core Infrastructure team, which ended up being a catch-all team for Squarespace’s infrastructure org.

Some projects included:

- An internal URL shortener used throughout the company.
- Migrating off of Bind DNS to Power DNS.
- General infrastructure gardening, including cleaning up Ansible scripts and finding and solving a bug where credentials were being indexed in an internal ElasticSearch instance.

Eventually, I moved to data infrastructure as part of a reorg since I had experience with Kafka

- Setting up simple cross datacenter replication for Kafka.
- Log ingestion and configurable monitoring for Redis, RabbitMQ, Kafka, and Couchbase.
- Find and solved a longstanding performance issue with Couchbase that led to multi-second 99th response times.

<br />

---

### Astronomer.io, Software Engineer

_June 2017 - February 2018_

Astronomer was my first full-time job out of college.
At the time, it was a seed-stage startup doing web analytics stuff but eventually pivoted to offering hosted Apache Airflow.

While working there I:

- Setup initial Prometheus monitoring and dashboards.
- Migrated Kinesis workers to Kafka.
- Wrote the code to automate the creation of the data storage layer for Astronomer's initial hosted Apache Airflow offering.

<br />

---

### RIT, Data mining Teaching Assistant

_January 2016 - May 2017_

After taking Principles of Data Mining, I was offered a job as a teaching assistant.
This meant a lot of grading, narking on cheaters, and running office hours for students to come in and ask questions.

<br />

---

### RIT, Research Assistant

_August 2015 - June 2016_

I worked at RIT’s Computational Biomedical Laboratory working on heart arrhythmias.
Work included converting Ph.D. students’ code from c++ to MatLab, assisting in coding statistical models, and scripting conversions between different data types for heart models.

<br />

---

### Hubspot, Software Engineer Co-op

_June 2016 - January 2017_

I worked on the data infrastructure team, with the focus of my coop being on HubSpot’s Apache Kafka instances handling millions of requests per second.
By the end of the coop, I was one of the few coops to be on their team’s pager rotation. Some projects I worked on included:

- Improving Ansible provisioning of Kafka to make new instance provisioning lower touch.
- Worked around a bug in Kafka 0.8 where a feature to reset a consumer to a particular point-in-time would use the log file mtime rather than the time the log segment was produced to reset the offset.
  This led to the Kafka API resetting the offset to an earlier offset than intended in a sufficiently large Kafka deployment. Our system indexed Kafka message offsets in Hbase and their creation time.
- A service that safely automated tasks like rolling restarts by using Monit to make API calls to instances while considering performance statistics and the state of the cluster
- A framework lint MySQL queries for common mistakes.
  I could only partially get started on this before my internship ended.

<br />

---

### iCitizen, Data Engineer Intern

_June 2015 - August 2015_

Built data visualization of voter campaign finance data to help voters better understand where a candidate’s funding comes from.
I took data from its raw form, cleaned it, transformed it, and then visualized it. Other duties include writing scripts that are used to ingest voter file data into databases.

<br />

---

### RIT, Research Computing Admin

_March 2014 - May 2014_

Maintained Linux systems used for researching the streaming of high-resolution video in a research environment.

<br />

---

### IDI Billing, QA Automation Intern

_June 2014 - December 2014_

Designed and developed an in-house framework used for automated web GUI and web service testing.
Logged application bugs and solved framework bugs

<br />
<br />
<br />

<table class="min-w-full text-center">
    <thead>
        <tr class="text-lg">
            <th>Education</th>
            <th>Awards</th>
            <th>Classwork</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="text-md font-semibold">
                Rochester Institute of Technology
            </td>
            <td>AMA Datafest Best Insight 2017</td>
            <td>Computer Graphics</td>
        </tr>
        <tr">
            <td>
                Rochester, New York
            </td>
            <td>Dean’s List Spring 2016</td>
            <td>Intelligent Systems</td>
        </tr>
        <tr>
            <td>B.Sc Computer Science, Cum Laude</td>
            <td>Dean’s List Spring 2015</td>
            <td>Functional Programming</td>
        </tr>
        <tr>
            <td></td>
            <td>Dean’s List Fall 2013</td>
            <td>Data Mining and Statistics</td>
        </tr>
        <tr>
            <td></td>
            <td>Dean’s List Spring 2013</td>
            <td>University Physics</td>
        </tr>
        <tr>
            <td></td>
            <td>CS Chess AI Tournament 1st Place 2012</td>
            <td>Linear Algebra</td>
        </tr>
        <tr>
            <td></td>
            <td>National Honor Society 2011</td>
            <td>Analysis of Algorithms</td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td>Programming Language Theory</td>
        </tr>
    </tbody>
</table>
