# Embedded systems: why build images instead of just dd'ing it?

## Introduction

When working with embedded systems, its common to burn pre-built images to the storage medium, and once you need to save the current state of the system, you just `dd` the storage medium to a file into an image that you can distribute and burn in other storage medium. This is a common practice, but it has some drawbacks. In this article, we will discuss why (sometimes) building images is a better approach.

## 
