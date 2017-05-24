# RQ Scheduler
*RQ Scheduler is a package that adds job scheduling capabilities to RQ.*


* What is RQ Scheduler?

  RQ Scheduler is a small package that adds job scheduling capabilities to RQ,
  a Redis based Python queuing library.

  For more info: https://github.com/ui/rq-scheduler

* What language is RQ written in?

  Python (v2.7)

* How do I create a Docker container?

  ```
     docker build -t rq-scheduler .
     docker run -d --name redis redis
     docker run -d --link redis:redis --name rq_scheduler rq-scheduler
  ```

  The scheduler process polls Redis every minute and moves scheduled
  jobs to the relevant queues when they need to be executed.
