# IPC: An IMAGE Data Set Compiled from International Planning Competitions

This repository provides the data set, named IPC, for the evaluation of machine learning methods on images. It contains two collections of labeled images, presplit for training/validation/testing. The labels correspond to a total time it takes each planner to solve the corresponding planning task, and the two collections correspond to lifted and grounded representations of planning tasks. For additional details on planners and images, see [Katz et al. (2018)](#Katz2018) and [(Sievers et al. 2019)](#Sievers2019). 

## <a id="background"></a>Background

Automated planning is one of the foundational areas of AI. Even the simplest formalism is known to be PSPACE-hard, and therefore no single planner can be expected to work well for all problems and domains. Thus, portfolio-based techniques has become increasingly popular. In particular, deep learning emerges as a promising methodology for online planner selection. A prominent example is the winner, *Delfi* [(Katz et al. 2018)](#Katz2018), of the Optimal Track of the [International Planning Competition (IPC) 2018](https://ipc2018.bitbucket.io).

The planner reasons about problems represented as images, constructed from structural graph representations of the planning problems [(Katz et al. 2018)](#Katz2018). Two examples are the *problem description graph* [(Pochter et al. 2011)](#Pochter2011) for a **grounded** representation, and the *abstract structure graph* [(Sievers et al. 2017)](#Sievers2017) for a **lifted** representation.

The file runtimes.csv describes the collection of planning tasks with time needed for solving each task, for a collection of 29 planners. These planners include the 17 planners in the portfolio of *Delfi*, as well as the planners that participated in IPC 2018. The details of some of the planners may be found in [Katz et al. (2018)](#Katz2018).

The timeout limit for each problem is 1800s. For planners that fail to solve the problem before timeout, the target value is artificially set as 10000.

The problems not solved by any of the planners in the portfolio within the timeout limit 1800s are ignored in the construction of the data set. In particular, some of these problems occur in IPC 2018. Hence, the test set contains problems strictly fewer than those in IPC 2018.

## File Format

There are two folders with images: `grounded` and `lifted`. Each of these folders contains a collection of images, named by the corresponding planning task. 

Additionally, the folder `problems` contains files with problem names, with one suggested separation to training/validation/test sets.

## Citing This Data Set

```
@InProceedings{sievers-et-al-aaai2019,
  author =       "Silvan Sievers, Michael Katz, Shirin Sohrabi, Horst Samulowitz, and Patrick Ferber",
  title =        "Deep Learning for Cost-Optimal Planning: Task-Dependent Planner Selection",
  booktitle =    "Proceedings of the Thirty-Third {AAAI} Conference on
                  Artificial Intelligence ({AAAI} 2019)",
  year =         "2019"
}

```

## Bibliography

- <a name="Katz2018"></a>Michael Katz, Shirin Sohrabi, Horst Samulowitz, and Silvan Sievers. [Delfi: Online planner selection for cost-optimal planning](https://ipc2018-classical.bitbucket.io/planner-abstracts/teams_23_24.pdf). In Ninth International Planning Competition (IPC-9): planner abstracts, 2018.
- <a name="Pochter2011"></a>Nir Pochter, Aviv Zohar, and Jeffrey S. Rosenschein. [Exploiting problem symmetries in state-based planners](http://icaps11.icaps-conference.org/proceedings/hdip/pochter-et-al.pdf). In AAAI, 2011.
- <a name="Sievers2017"></a>Silvan Sievers, Gabriele Röger, Martin Wehrle, and Michael Katz. [Structural symmetries of the lifted representation of classical planning tasks](http://ai.cs.unibas.ch/papers/sievers-et-al-icaps2017wshsdip-a.pdf). In ICAPS 2017 Workshop on Heuristics and Search for Domain-independent Planning, 2017.
- <a name="Sievers2019"></a>Silvan Sievers,  Michael Katz, Shirin Sohrabi, Horst Samulowitz, and Patrick Ferber. [Deep Learning for Cost-Optimal Planning: Task-Dependent Planner Selection](). In The Thirty-Third AAAI Conference on Artificial Intelligence (AAAI-19), 2019.


## Contributors (In Alphabetical Order)

- Patrick Ferber, University of Basel
- Michael Katz, IBM Research
- Horst Samulowitz, IBM Research
- Silvan Sievers, University of Basel
- Shirin Sohrabi, IBM Research

## Contact

Please direct questions to Michael Katz, michael.katz1@ibm.com.
