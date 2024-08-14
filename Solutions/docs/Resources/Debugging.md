## Complexity in System Performance

- **Complexity**: Symptoms are often far removed from the root cause.
- **Multiple Causes**: There may be several contributing factors.
- **Dynamic Nature**: Systems can change unexpectedly.
- **Modeling and Verification**: Improvements are difficult to model and verify.

**Note**: This isn’t tuning; it's debugging. You tune an instrument; you debug a system once you understand it.

## Debugging Pathologically Performing Systems

When approaching system performance issues as debugging, we must recognize that understanding and fixing them is neither rote nor easy.

- **Avoid relying on anecdotes**: Just because a problem occurred once doesn't mean it's the cause now.
- **Don't make changes without understanding**: Just as you wouldn't debug code by changing it randomly, don't alter a system without knowing the root cause.

## Essential Skills for Effective Debugging

- **Critical Thinking**: Recognize that understanding and fixing system performance issues require thoughtful analysis.
- **Skepticism**: Avoid the temptation to rely on anecdotal evidence or folklore.
- **Patience and Diligence**: Take the time to thoroughly understand the system before making changes.
- **Methodical Approach**: Emphasize the importance of a structured and reasoned approach to debugging.

## Methodical Debugging Process

To debug methodically, resist the temptation to jump to quick hypotheses and instead focus on questions and observations.

- **Iterate between questions and observations**: Gather facts that will constrain future hypotheses.
- **Disconfirm hypotheses**: Use gathered facts to disconfirm false hypotheses.
- **Question and Observe**:
  - How should we ask questions?
  - How should we make observations?

## Starting Points for Debugging

Where does one start?

- **Resource-centric methodologies**: Methods like the USE Method (Utilization/Saturation/Errors) can be excellent starting points.
- **Contextual Application**: Remember to keep these methodologies in context—they provide initial questions to ask but are not comprehensive recipes for debugging all performance issues.

## Importance of Observability

Observability is crucial; without it, you'll be left guessing and making inferences.

- **Questions are answered through observation.**
- **The system's observability is paramount.**
- **Without observability**, you're reduced to guessing, making changes, and drawing inferences.
- **Correlation does not imply causation**: Drawing inferences based solely on changes is flawed.
- **Instrumental systems**: For a system to be observable, it must be capable of emitting data as needed.

## Methods of Instrumentation

Once we determine what is visible, we need to talk about the methods of instrumentation involved in adding code to a system to collect useful data. It can be categorized into two types: static and dynamic.

- **Static Instrumentation**: Modifies the source code to provide semantically relevant information, such as through logging or counters. It is essential for gathering observations necessary for formulating initial questions.
- **Dynamic Instrumentation**: Allows for changes to be made to the system while it is running, enabling it to emit data on demand. It is crucial for answering deeper, ad hoc questions.

Both static and dynamic instrumentation are essential for comprehensive system monitoring and analysis.
