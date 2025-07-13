# What is EBPF?

A debugger on Linux kernel

## What are we building?

A stealthy debugger that can record unexpected file operation done in a project directory which indeed can detect the vulnerabilities if container process is able to access certain file in a non intended way

So it is basically container testing tool to detect file access which was not suppose to happen

## Why a container testing tool?

There is a single tool that can do everything from file monitoring to network monitoring. That is falco

We do not get a specific tool for actual file testing or we get tools that do not work on container. Here are some example fanotify and auditctl

Testing is usually preferred on low end hardware so building is specifically for k3s may be good as k3s is basically light weight kubernetes

This is would help the user of this product to actually see how much is their container Harding actually working

Here is a rough architecture of the project
