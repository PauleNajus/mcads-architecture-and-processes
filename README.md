# MCADS Architecture and Processes

## Table of content

- [List of figures](#list-of-figures)
- [Introduction](#introduction)
- [BPMN](#bpmn)
- [C4](#c4)
- [DFD](#dfd)
- [Rich picture](#rich-picture)
- [Structural diagrams](#structural-diagrams)
- [UML](#uml)

## List of figures

1. Figure 1: BPMN MCADS process - main
2. Figure 2: MCADS-BPMN tests and comparison process (part A)
3. Figure 3: MCADS-BPMN tests and comparison process (part B)
4. Figure 4: MCADS-C4 level 1 context
5. Figure 5: MCADS-C4 level 2 container
6. Figure 6: MCADS-C4 level 3 component ml
7. Figure 7: MCADS-C4 level 3 component web app
8. Figure 8: MCADS-DFD level 0
9. Figure 9: MCADS-DFD level 1
10. Figure 10: MCADS-DFD level 2 inference
11. Figure 11: MCADS-DFD level 2 interpretability
12. Figure 12: MCADS-DFD level 2 segmentation
13. Figure 13: MCADS-DFD level 2 upload
14. Figure 14: MCADS-DFD level 3 classification
15. Figure 15: MCADS-DFD level 3 gradcam
16. Figure 16: MCADS-Rich picture problem
17. Figure 17: MCADS-Rich picture solution
18. Figure 18: MCADS-Rich picture system architecture
19. Figure 19: MCADS-Information Architecture diagram
20. Figure 20: MCADS-UML activity workflow
21. Figure 21: MCADS-UML class diagram
22. Figure 22: MCADS-UML component
23. Figure 23: MCADS-UML deployment
24. Figure 24: MCADS-UML Interactions Diagram
25. Figure 25: MCADS-UML object
26. Figure 26: MCADS-UML package
27. Figure 27: MCADS-UML sequence interpretability
28. Figure 28: MCADS-UML sequence upload inference
29. Figure 29: MCADS-UML state machine
30. Figure 30: MCADS-UML use case diagram

## Introduction

This repository contains the architecture and process diagrams for the MCADS (Multi-Label Chest Abnormality Detection System) project. The diagrams are categorized into various standard modeling languages and frameworks to provide a comprehensive view of the system from different perspectives, including business processes, system context, data flow, and structural design.
MCADS prototype can be reached here: <https://mcads.cloud/accounts/login/?next=/> ; username: “guest”; password: “GuEst2025!”.
MCADS source code can be reached here: <https://github.com/PauleNajus/mcads/tree/prod> .
Raw testing logs, evaluation metrics, and comparative graphs of 7 models used in MCADS can be reached here: <https://github.com/PauleNajus/mcads-model-evaluations> .

## BPMN

Business Process Model and Notation (BPMN) diagrams illustrating the main workflows and testing processes of the MCADS system.

### BPMN MCADS process - main

This diagram illustrates the end-to-end business process of the Multi-Label Chest Abnormality Detection System (MCADS). It maps out the user journey from initial image acquisition and upload, through the automated analysis phases, to the final diagnostic review by a medical professional.

![BPMN MCADS process - main](./BPMN/BPMN%20MCADS%20process%20-%20main.png)

Figure 1: BPMN MCADS process - main

### MCADS-BPMN tests and comparison process (part A)

This diagram details the first phase of the testing and evaluation process for the machine learning models used in MCADS. It covers the data preparation, model training, and initial validation steps required to benchmark different diagnostic algorithms.

![MCADS-BPMN tests and comparison process (part A)](./BPMN/MCADS-BPMN%20tests%20and%20comparison%20process%20(part%20A).png)

Figure 2: MCADS-BPMN tests and comparison process (part A)

### MCADS-BPMN tests and comparison process (part B)

Continuing from Part A, this diagram outlines the subsequent steps in the model evaluation process. It focuses on the comparative analysis of model performance metrics, statistical testing, and the final selection criteria for deploying the best-performing model into the production environment.

![MCADS-BPMN tests and comparison process (part B)](./BPMN/MCADS-BPMN%20tests%20and%20comparison%20process%20(part%20B).png)

Figure 3: MCADS-BPMN tests and comparison process (part B)

## C4

C4 model diagrams providing a hierarchical view of the software architecture, from high-level context down to specific components.

### MCADS-C4 level 1 context

The System Context diagram provides a high-level overview of MCADS, illustrating how the system interacts with its primary users (such as radiologists and patients) and any external systems or third-party services it relies upon.

![MCADS-C4 level 1 context](./C4/MCADS-C4%20level%201%20context.png)

Figure 4: MCADS-C4 level 1 context

### MCADS-C4 level 2 container

This Container diagram breaks down the MCADS architecture into its major deployable units. It shows the interactions between the web application frontend, the backend API, the machine learning inference service, and the underlying databases used for storing user and image data.

![MCADS-C4 level 2 container](./C4/MCADS-C4%20level%202%20container.png)

Figure 5: MCADS-C4 level 2 container

### MCADS-C4 level 3 component ml

Focusing specifically on the Machine Learning container, this Component diagram details the internal software components responsible for image preprocessing, abnormality segmentation, classification, and generating interpretability visualizations.

![MCADS-C4 level 3 component ml](./C4/MCADS-C4%20level%203%20component%20ml.png)

Figure 6: MCADS-C4 level 3 component ml

### MCADS-C4 level 3 component web app

This Component diagram dives into the Web Application container, outlining the internal modules such as user authentication, image upload handling, result rendering, and communication interfaces with the backend services.

![MCADS-C4 level 3 component web app](./C4/MCADS-C4%20level%203%20component%20web%20app.png)

Figure 7: MCADS-C4 level 3 component web app

## DFD

Data Flow Diagrams (DFD) mapping the flow of information through the MCADS system at various levels of detail.

### MCADS-DFD level 0

The Context Data Flow Diagram shows the MCADS system as a single process, highlighting the incoming data flows (e.g., user credentials, chest X-ray images) and outgoing data flows (e.g., diagnostic reports, visualizations) to and from external entities.

![MCADS-DFD level 0](./DFD/MCADS-DFD%20level%200.png)

Figure 8: MCADS-DFD level 0

### MCADS-DFD level 1

This Level 1 DFD decomposes the main system into its primary sub-processes, such as user management, image upload, inference, and result generation, illustrating the data stores and data flows connecting them.

![MCADS-DFD level 1](./DFD/MCADS-DFD%20level%201.png)

Figure 9: MCADS-DFD level 1

### MCADS-DFD level 2 inference

This diagram provides a closer look at the inference process, tracing the flow of image data as it is fed into the machine learning models and how the resulting predictions are structured and stored.

![MCADS-DFD level 2 inference](./DFD/MCADS-DFD%20level%202%20inference.png)

Figure 10: MCADS-DFD level 2 inference

### MCADS-DFD level 2 interpretability

Detailing the interpretability pipeline, this DFD shows how classification results and original images are processed to generate explainable AI outputs, helping users understand the model's decision-making process.

![MCADS-DFD level 2 interpretability](./DFD/MCADS-DFD%20level%202%20interpretability.png)

Figure 11: MCADS-DFD level 2 interpretability

### MCADS-DFD level 2 segmentation

This diagram maps the data flow specific to the image segmentation task, showing how raw images are processed to isolate the region of interest from the background before classification.

![MCADS-DFD level 2 segmentation](./DFD/MCADS-DFD%20level%202%20segmentation.png)

Figure 12: MCADS-DFD level 2 segmentation

### MCADS-DFD level 2 upload

This DFD illustrates the data flow during the image upload process, including validation, format conversion, and initial storage mechanisms.

![MCADS-DFD level 2 upload](./DFD/MCADS-DFD%20level%202%20upload.png)

Figure 13: MCADS-DFD level 2 upload

### MCADS-DFD level 3 classification

A highly granular Level 3 DFD that breaks down the classification component, showing the exact data transformations and feature extractions that occur within the neural network layers.

![MCADS-DFD level 3 classification](./DFD/MCADS-DFD%20level%203%20classification.png)

Figure 14: MCADS-DFD level 3 classification

### MCADS-DFD level 3 gradcam

This detailed Level 3 DFD maps the specific data operations required to compute Gradient-weighted Class Activation Mapping (Grad-CAM) visualizations, which highlight the regions of the image most influential to the model's prediction.

![MCADS-DFD level 3 gradcam](./DFD/MCADS-DFD%20level%203%20gradcam.png)

Figure 15: MCADS-DFD level 3 gradcam

## Rich picture

Rich pictures providing an informal, holistic view of the problem situation, the system architecture, and the proposed solution.

### MCADS-Rich picture problem

This rich picture provides an informal, holistic view of the real-world challenges in chest abnormality diagnosis, such as the need for early detection, the shortage of specialized radiologists, and the potential for human error.

![MCADS-Rich picture problem](./Rich%20picture/MCADS-Rich%20picture%20problem.png)

Figure 16: MCADS-Rich picture problem

### MCADS-Rich picture solution

This diagram depicts how MCADS addresses the identified problems by integrating AI-assisted analysis into the clinical workflow, ultimately supporting doctors in making more accurate and timely diagnoses.

![MCADS-Rich picture solution](./Rich%20picture/MCADS-Rich%20picture%20solution.png)

Figure 17: MCADS-Rich picture solution

### MCADS-Rich picture system architecture

A conceptual and user-friendly illustration of the MCADS architecture, showing how different hardware and software components interact within the clinical environment.

![MCADS-Rich picture system architecture](./Rich%20picture/MCADS-Rich%20picture%20system%20architecture.png)

Figure 18: MCADS-Rich picture system architecture

## Structural diagrams

Diagrams focusing on the static structure and organization of the system's information.

### MCADS-Information Architecture diagram

This diagram outlines the structural design of the MCADS application's information space. It maps the site navigation, page hierarchies, and content organization to ensure a logical and intuitive user experience.

![MCADS-Information Architecture diagram](./Structural%20diagrams/MCADS-Information%20Architecture%20diagram.png)

Figure 19: MCADS-Information Architecture diagram

## UML

Unified Modeling Language (UML) diagrams providing standardized representations of the system's design, behavior, and structure.

### MCADS-UML activity workflow

This Activity diagram models the dynamic behavior of the system by showing the sequence of user and system activities, decision points, and parallel processing steps during a typical diagnostic session.

![MCADS-UML activity workflow](./UML/MCADS-UML%20activity%20workflow.png)

Figure 20: MCADS-UML activity workflow

### MCADS-UML class diagram

The Class diagram defines the static structure of the MCADS software, detailing the key classes (e.g., User, Image, Prediction, Model), their attributes, methods, and the relationships between them.

![MCADS-UML class diagram](./UML/MCADS-UML%20class%20diagram.png)

Figure 21: MCADS-UML class diagram

### MCADS-UML component

This Component diagram illustrates the physical structure of the software system, showing the dependencies and interfaces between various software modules, libraries, and executables.

![MCADS-UML component](./UML/MCADS-UML%20component.png)

Figure 22: MCADS-UML component

### MCADS-UML deployment

The Deployment diagram maps the software artifacts onto the physical hardware infrastructure, showing how the web servers, database servers, and ML inference nodes are distributed and connected in the production environment.

![MCADS-UML deployment](./UML/MCADS-UML%20deployment.png)

Figure 23: MCADS-UML deployment

### MCADS-UML Interactions Diagram

This diagram provides a broad view of the interactions between different system components and actors, emphasizing the flow of control and data during complex operations.

![MCADS-UML Interactions Diagram](./UML/MCADS-UML%20Interactions%20Diagram%20.png)

Figure 24: MCADS-UML Interactions Diagram

### MCADS-UML object

An Object diagram that captures a snapshot of the system at runtime, showing specific instances of classes and their current states and relationships during an active diagnostic session.

![MCADS-UML object](./UML/MCADS-UML%20object.png)

Figure 25: MCADS-UML object

### MCADS-UML package

This Package diagram illustrates how the MCADS codebase is organized into logical namespaces and modules, highlighting the dependencies between different architectural layers.

![MCADS-UML package](./UML/MCADS-UML%20package.png)

Figure 26: MCADS-UML package

### MCADS-UML sequence interpretability

A Sequence diagram that details the chronological order of messages and method calls exchanged between objects when a user requests interpretability visualizations (like Grad-CAM) for a specific prediction.

![MCADS-UML sequence interpretability](./UML/MCADS-UML%20sequence%20interpretability.png)

Figure 27: MCADS-UML sequence interpretability

### MCADS-UML sequence upload inference

This Sequence diagram traces the exact timeline of interactions from the moment a user uploads an image, through the backend processing and ML inference, to the return of the diagnostic results.

![MCADS-UML sequence upload inference](./UML/MCADS-UML%20sequence%20upload%20inference.png)

Figure 28: MCADS-UML sequence upload inference

### MCADS-UML state machine

The State Machine diagram models the lifecycle of a key entity, such as an uploaded image, showing its various states (e.g., Uploaded, Preprocessing, Analyzing, Completed, Failed) and the events that trigger state transitions.

![MCADS-UML state machine](./UML/MCADS-UML%20state%20machine.png)

Figure 29: MCADS-UML state machine

### MCADS-UML use case diagram

This Use Case diagram identifies the primary actors (e.g., Medical Professional, System Administrator) and their respective interactions with the system, summarizing the core functional requirements of MCADS.

![MCADS-UML use case diagram](./UML/MCADS-UML%20use%20case%20diagram.png)

Figure 30: MCADS-UML use case diagram
