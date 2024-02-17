# Spring Updates 2023
*Date: June 2023*

## Classes

This quarter, I took Data Structures and Parallelism (which is UW's unique version of DSA), The Hardware Software Interface, and a career seminar on succeeding in the tech industry. In my Data Structures and Parallelism course, I completed several large projects where I implemented various data structures from scratch, all without using any classes in the java.util library. We also took a deep dive on parallelism and concurrency, as well as graph algorithms like Prim's, Kruskal's, Dijkstra's, and various others.

Unfortunately, I also had to learn a fair bit of x86 Assembly, but my growing understanding of computer hardware and architecture has been a guiding light at the end of this tunnel. This class (HSI) has really solidified my understanding of C. Some of my favorite topics from this course were learning cache-aware programming to optimize array/matrix algorithms, and processes/scheduling and concurrency using fork/exec in C. The class also wrapped up with a comparison between the implementation details of Java and C, which was super interesting.

## Projects

We finally finished our MVP for Syntext, and have deployed our site! Now we are working on the interesting parts of the backend which is super exciting. So far we've implemented user accounts and authentication, and are currently working on a spec for our leaderboard API.

Implementing a leaderboard has posed to be a very interesting systems design question. Although I doubt we will ever have more than a few hundred people on the leaderboard, I still want to make the leaderboard highly scalable and efficient. I've done a lot of research into different storage solutions for real-time updates, and am considering either maintaining a leaderboard in-memory with user-ids on the server, or using a Redis sorted set to automatically update based on new POST requests to the server. At the end of the day however, a big factor in this design decision will be the price.

Besides my work with Syntext, I have also been coding for an RSO here at UW called Nexus. I joined this group well after the MVP was finished, but I've found this has been good practice working on an already established codebase (something that is necessary in industry). So far I've implemented a few features, such as email verification and an application summary page, and have also been working on bug-fixes while waiting on more feedback/mockups from the design and UX teams. Working in a group with a dedicated UX/design team is definitely a new experience for me, but I am liking the fact that I don't have to come up with the style on my own, instead just trying to match whatever the Figma mock-ups look like.

I recently won my first hackathon (DevMatch June 2023), and am super happy I had the opportunity to participate. It was a little different from most hackathons I've partaken in, as we were tasked with fixing bugs in an existing codebase. I ended up scoring the highest in terms of the number of bugs fixed within the time limit.

I also recently started my first SWE internship, and have really deepened my understanding of the Java web ecosystem. Although server-side development with core Java (Servlets API) has proven to be much slower, I've learned a ton due to the lack of abstracted complexity compared to using a framework like SpringBoot.

## Goals

This quarter, my goal was to enhance my knowledge of software design patterns. To achieve this, I have been studying "Effective Java" by Joshua Bloch. Through my readings, I have familiarized myself with various design patterns such as Singletons, Prototypes, Adapters, and Observers. Though I have yet to use these patterns in my code, I have found it fascinating to discover how popular frameworks like React and SpringBoot implement them. Among the patterns I've studied, the Observer pattern has intrigued me the most.

In addition, I aimed to start contributing to open-source projects that I use. Recently, I made my first "real" contribution by addressing an issue in the node-mysql2 module's GitHub repository. As a frequent user of the module for Syntext, I noticed that it only implemented error codes from the latest release of MySQL 5.7, even though MySQL 8.0 had introduced many new error codes. To solve this, I modified the current error generator used in mysql2 to scrape the new source code for MySQL 8.0. I then submitted a pull request with the updated error codes and integration tests to ensure the codes were thrown in the correct circumstances. Although I felt intimidated by working with such large codebases, submitting my first pull request to a repository utilized by thousands of developers was exhilarating.
