# Reflexion Pipeline

This project implements a Reflexion Pipeline, which allows for iterative task refinement and evaluation. <br>
this file can be used as a module in your own computer <br>
just clone the repo and use the file path as a module(better keep this file in your directory where you are trying to import it) <br>
still a work in progress a lot of optimizations and work is in progress <br>

## Usage

Here's a basic example of how to use the Reflexion Pipeline:

``` 
from reflexion import ReflexionPipeline

# Initialize the pipeline with a model name
reflexion = ReflexionPipeline(model_name)

# Define your task
task =""

# Run the reflexion loop
final_task, final_output, final_evaluation = reflexion.reflexion_loop(task, max_iterations=5, criteria=0.9)

```

## Parameters

* `model_name`: The name of the model to use for the Reflexion Pipeline.
* `task`: The initial task or prompt to refine and evaluate.
* `max_iterations`: The maximum number of iterations for the reflexion loop (default is 5).
* `criteria`: The exit criteria score (between 0 and 1) at which the loop will stop if reached before max_iterations (default is 0.9).

## Customization

You can customize the Reflexion Pipeline by adjusting the following parameters:

* `max_iterations`: Set this to the number of reflexion iterations you want to perform.
* `criteria`: Adjust this value to change the satisfactory score at which the loop will exit early.

## Output

The `reflexion_loop` method returns three values:

1. `final_task`: The refined task after iterations.`
2. `final_output`: The final output generated for the task.
3. `final_evaluation`: The evaluation score for the final output.

## Note

Make sure to define your `task` variable with an appropriate prompt or task description before running the reflexion loop.
