# Concurrency Library for ColdFusion

## Overview

This repository provides a library for implementing concurrent processing in ColdFusion applications. It includes a set of components designed to manage tasks that can run concurrently, improving the performance and efficiency of ColdFusion applications.

## Features

- **Task Management**: Create and manage tasks that run concurrently.
- **Future Events**: Handle future events that can be executed asynchronously.
- **Callable Interface**: Define tasks with a standardized interface for execution.
- **Task Pools**: Manage a pool of tasks that can be executed concurrently.
- **Task Vectors**: Handle collections of tasks and manage their execution order.

## Installation

To install the Concurrency library:

1. Clone this repository to your ColdFusion server:
   ```bash
   git clone https://github.com/Squid2112/Concurrency.git
   ```

## Include the necessary components in your ColdFusion application:

- **Callable.cfc**
- **FutureEvent.cfc**
- **FutureTask.cfc**
- **TaskPool.cfc**
- **TaskVector.cfc**

## Usage
Basic Example
Here is a simple example of how to use the TaskPool and FutureTask components:
```<cfset taskPool = new TaskPool()>
<cfset futureTask1 = new FutureTask(new Callable(function() { return "Task 1"; }))>
<cfset futureTask2 = new FutureTask(new Callable(function() { return "Task 2"; }))>

<cfset taskPool.addTask(futureTask1)>
<cfset taskPool.addTask(futureTask2)>

<cfset results = taskPool.executeAll()>
<cfoutput>#results#</cfoutput>
```

## Components
- **Callable.cfc**: Defines a standard interface for tasks that can be executed.
- **FutureEvent.cfc**: Manages events that are scheduled to run in the future.
- **FutureTask.cfc**: Handles individual tasks that can be executed asynchronously.
- **TaskPool.cfc**: Manages a pool of concurrent tasks.
- **TaskVector.cfc**: Handles a collection of tasks and their execution.

