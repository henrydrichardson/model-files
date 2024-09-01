**Overview**
===============

This code is a template for generating commit messages using a specific format. It takes input from various sources, such as user input and tool calls, and produces a formatted response based on the provided parameters.

**Functionality**
================

The code uses Go templates to generate HTML responses. The functionality can be broken down into several sections:

### Writing Commit Messages

* When writing commit messages, the code checks if there are any changes to report.
* If there are changes, it summarizes them and lists the affected files and changes made.

### Tool Calls

* When receiving a tool call response, the code uses the output to format an answer to the original use question.
* It also responds in JSON format with the name of the function called and its arguments.

### Variables

The code uses several variables:

* `.Messages`: An array of messages to be written
* `.System`: A variable representing the system being used (e.g., Git)
* `.Tools`: A variable containing tool call responses
* `.Role`: A variable indicating the role being played (user, assistant, or tool)
* `.Content`: The content of the message or response
* `.Prompt`: The prompt or question being asked

### Dependencies

This code does not have any external dependencies.

### Assumptions

The code assumes that:

* Input data is in a specific format (e.g., JSON for tool calls)
* Environmental conditions are suitable for generating commit messages and responding to tool calls

**Variables**
=============

| Variable | Type | Scope | Description |
| --- | --- | --- | --- |
| `.Messages` | array | global | An array of messages to be written |
| `.System` | string | global | A variable representing the system being used (e.g., Git) |
| `.Tools` | object | global | A variable containing tool call responses |
| `.Role` | string | global | A variable indicating the role being played (user, assistant, or tool) |
| `.Content` | string | local | The content of the message or response |
| `.Prompt` | string | local | The prompt or question being asked |

**Dependencies**
===============

None

**Assumptions**
==============

* Input data is in a specific format (e.g., JSON for tool calls)
* Environmental conditions are suitable for generating commit messages and responding to tool calls

**Inspirations/Credits**
==============

* This modelFile was highly inspired by [Harper Reed's generate meaningful git commit messages](https://harper.blog/2024/03/11/use-an-llm-to-automagically-generate-meaningful-git-commit-messages/)
