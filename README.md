# Missy Bernskoetter 2/28/2023
# streaming-04-multiple-consumers

> Use RabbitMQ to distribute tasks to multiple workers

One process will create task messages. Multiple worker processes will share the work. 


## Before You Begin

1. Fork this starter repo into your GitHub.
1. Clone your repo down to your machine.
1. View / Command Palette - then Python: Select Interpreter
1. Select your conda environment. 

## Read

1. Read the [RabbitMQ Tutorial - Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)
1. Read the code and comments in this repo.

## RabbitMQ Admin 

RabbitMQ comes with an admin panel. When you run the task emitter, reply y to open it. 

(Python makes it easy to open a web page - see the code to learn how.)

## Execute the Producer

1. Run emitter_of_tasks.py (say y to monitor RabbitMQ queues)

Explore the RabbitMQ website.

## Execute a Consumer / Worker

1. Run listening_worker.py

Will it terminate on its own? How do you know? 
No it will not, it is continuous and requires control+c to exit. Also, the prefetch_count=1 so it will continue

## Ready for Work

1. Use your emitter_of_tasks to produce more task messages.

## Start Another Listening Worker 

1. Use your listening_worker.py script to launch a second worker. 

Follow the tutorial. 
Add multiple tasks (e.g. First message, Second message, etc.)
How are tasks distributed? Depending on which one you ran the listening worker python file on first.
Monitor the windows with at least two workers. 
Which worker gets which tasks?
Each one gets a task based on the distribution. While the first worker got the first task, the second worker got the second. This looks different on mine because I ran v1 for the first task and v2 for the sencond-fifth task. So for mine it looks like the first worker got the second and fourth task and the second worker got the third and fifth task.


## Reference

- [RabbitMQ Tutorial - Work Queues](https://www.rabbitmq.com/tutorials/tutorial-two-python.html)


## Screenshot

See a running example with at least 3 concurrent process windows here:

[Concurrent terminal](Concurrent_Terminals.JPG)

[Queues](Queues.JPG)

These images are from the original v2 run

[v3_terminals](v3_terminals.JPG)