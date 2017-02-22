# Measure runtime of a function

I wanted to measure the runtime of a function - and a part of a function. I found the **Stopwatch Component** of Symfony and it does all i need.
 
    $stopwatch = new Stopwatch();
    // Start event named 'applyMcsUrl'
    $stopwatch->start('applyMcsUrl');
    // ... some code goes here
    $event = $stopwatch->stop('applyMcsUrl');
    // get total duration
    $timeTaken = $event->getDuration();

## Measure runtime in a Symfony application

It's not hard to measure the runtime inside a Symfony application - because Stopwatch is a component.
And it is already part of a basic Symfony application - and it's been shown in the Symfony profiler. 

    $stopwatch = $this->getContainer()->get('debug.stopwatch');
    $stopwatch->start('applyMcsUrl');
    // ...
    $stopwatch->stop('applyMcsUrl');

The result can be found in the profiler:

![Symfony profiler][2]

## Via

[Stopwatch - Symfony component][1]

[1]: http://symfony.com/doc/current/components/stopwatch.html
[2]: measure-runtime-of-a-function.jpg