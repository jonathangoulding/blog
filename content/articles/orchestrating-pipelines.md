---
title: Orchestrating pipelines
description: How to orchestrate software for local development and inside a gitlab ci pipeline

---

# Orchestrating pipelines

I am currently working towards an orchestated docker system
using gitlab ci to
make composable gitlab ci jobs that can be used through multiple project.
The jobs (mainly test) can pull the orechestraion repository and use the docker
compose to stand up the system
in order to test it in the pipeline.
