# [Testing of a robotic assembly workstation for the production of acoustic panels at Silen OÜ]

## Summary
| Company Name | [Silen OÜ](https://silen.com/en) |
| :--- | :--- |
| Development Team Lead Name | [Martinš Sarkans, PhD](https://www.etis.ee/CV/Martins_Sarkans/eng/) |
| Development Team Lead E-mail | [martins.sarkans@taltech.ee](mailto:martins.sarkans@taltech.ee) |
| Duration of the Demonstration Project | 01.12.2024 - 30.04.2025 |
| Final raport | [Final Raport.pdf] |
| Link to ETIS | [Project](https://www.etis.ee/Portal/Projects/Display/024c846b-dbcd-422a-81e6-e6a0ef79ed4b) |

# Description

## Objectives of the Demonstration Project

The aim of the demonstration project is to test the process of robotic screw fastening of acoustic panels with different configurations, considering the different dimensions of the panels, the number of screws to be installed and their installation. Considering the number of silence rooms to be produced and the projected increase in production volume, it is important to shorten the production time. One of the possible ways of achieving this is to move towards automation-robotic production.

This demonstration project links robotics (UR10 collaborative robot), automation (screw feeder, automatic screwdriver, intelligent jig), AI tools (digital workstation, machine vision tools, robot trajectory simulation).

Although many components are available separately on the market, there is no comprehensive solutions (integration) and methodology to make it fit to the company’s processes. The solution will consider the company’s specific production processes and requirements for the parameters of the acoustic panels, as well as the possibilities for implementing fully automated production (batch production) in the company or for deployment in other companies in the sector. Possible expected results: realization of a product assembly operation in the company, development of an assembly cell concept, selection of a suitable robot to carry out the assembly operation, selection of tools, simulation and testing.

## Activities and Results of the Demonstration Project
Main activities of the project:
1. Analysis of the current situation in the company and specification of the technical task (how the product is linked to the production flow, how the product is assembled, the time needed to assemble it, assessment of the possibilities for robotisation).
2. Development of a robotic assembly (screwing) workstation concept and definition of a specific application in the company (design of a robotic system in a simulation environment, selection of robot and instruments, proposal of an assembly cell concept).
3. Use of machine vision to achieve flexibility and increased production capacity (in screwing, this is the approach needed to identify hole locations).
4. Realisation of the prototype (Test Before Invest) solution in the company and its testing (robot + product + cell simulation in a virtual environment, system assembly in the company, testing of the robot and accessories).
5. Analysis of test results and validation of results (collection of data on the results of the demo project, analysis of the data, proposals for further development).
6. Drafting a general description of the concept of the central business solution (describing the solution in terms of the product and the business process and completing the simulation).
7. Publication of the results of the demo project and preparation of the project documentation.

### Challenges

One of the challenges that this demonstration project aims to address is the robotic production of acoustic panels to shorten the manufacturing time. As the assembly of acoustic panels is one of the most important and labor-intensive steps in the production process, the total time required to manufacture the product is directly related to the performance of the workstation.

### Activities implemented and results achieved

The first step was to analyze the current situation in the company and specify the technical task. This involved an analysis of the production feasibility, the nature and feasibility of the assembly process, the performance of the assembly workplace in relation to the product to be assembled (wall panel assembly). A time model for calculating and evaluating the duration of the production cycle for the product has been drawn up.

In the second phase, the development of a robotic assembly (screwing) workstation concept and the simulation of the screwing process were carried out. The development of the robotic screwing concept was based on a 3D model of the real product with the identification of the coordinates of the positions of the holes to be screwed. A simulation model was developed with real components (robot - UR 10e, robotic screwdriver OPTIMO Robotics S1 screwdriving system) and the use of models.

In the third phase, physical testing of the robotic screwdriving application was carried out. The test solution showed that robotic screwdriving was successful for the given materials, the correct working parameters were selected, and a high-quality result was achieved. The physical robotic screwdriving process proved that fast, accurate and high quality screwdriving can be achieved in every screwdriving cycle.

Fourth, the concept of a robotic workplace was developed. This activity was not part of the project plan, but it helped to get a better overview of the whole panel production.
The fifth step concerned the development and analysis of the production system (not part of the demo project), but as the workstation is an important part of the production system, it was inevitably briefly covered. The aim was to understand the production position plan and to analyze the nature of production flows.

In the sixth phase, the possibilities of AI were tested, which included the use of machine learning to achieve flexibility and increased production capacity. At the wall panel assembly workstation, it is necessary to identify the type, location and coordinates of the product to provide the collaborative robot with the necessary parameters to generate and run the screwing program. In this case, the product is a plate of a given shape with machined holes for screws.

Stage 7 consisted of validation and testing, where the virtual and real workplace were tested according to the plan. The prototype (Test Before Invest) solution was implemented and tested. For the simulation, a system solution was created in the RoboDK environment, consisting of the following components: the Optimo S1 screwdriving unit, the Universal Robot UR20 collaborative robot, the Optimo S1 screw feeding unit, the jig for wall panel installation and rotation, the wall panel model.


### Data Sources

For implementation of the project, research articles in this field were studied and analyzed. In addition, the following software solutions were used:
1. Cognex In-Sight Explorer for machine vision testing
2. RoboDK simulation software for robot application testing, simulation and program generation
3. Visual Components software for workplace layout preparation, simulation and flow verification
4. Universal Robots (UR) virtual machine (on Oracle VirtualBox) for robot program simulation and program generation
5. SolidWorks CAD software for intelligent fixture design and concept development
6. Python programming language for creation and generation of robot parametric programs in RoboDK

The following data was gathered during the project for the analysis and verification:
- production data, process information (time for assembly of acoustic panels)
- production floor layout plan for preparation of the simulation 
- machine vision data (Picture data of the products and their features) for training the model for product recognition and program generation
- product data for creation of the robot´s parametric programs

The algorithm for generating a program for the robot and the principles for defining the robot system's trajectory are given below. Stages:
-	Identifying the location of holes in the 3D model
-	Generation of a coordinate file based on the location of the holes
-	Determining the location of the coordinates of the points of intersection from the coordinate system
-	Importing the coordinates of the holes into the simulation environment.
-	Generation of programs based on points
-	Program simulation, training and verification

For the Machine Vision training following data was gathered about the product: as the holes for the screws are machined in a specific pattern, which provides the basis for generating the robot program. By transferring the image program to the Cognex In-Sight Explorer system, the corresponding detection algorithms can be added, such as: Product presence check; Horizontal edge detection; Vertical edge detection; Edge intersection detection (basis for program zero coordinate); Hole 1 detection; Hole 2 detection; Hole 1 distance from edge; Hole 2 distance from edge. For the training, the dataset of product specific Pictures was used.


### AI Technologies

For each stage of the project, a detailed description has been documented, the necessary simulations have been carried out, test data have been collected (screwing data, measurement and detection data, assembly data). The solutions have been tested and verified at different stages of the project. These are the following results:
-	physical testing for robotic screwing has been carried out, data collection, technical solution suitability assessment.
-	automatic generation of the robot program in a simulation environment, based on a Python script for generating the code, testing of the solution's functionality.
-	testing machine vision functionality, collection of data on the product, evaluation of the suitability of different detection algorithms, testing of the performance of machine vision solution on a real test set-up.
-	carried out a workstation reconfiguration in the simulation model, created a new workstation layout, designed a cell for product positioning, tested the suitability of the cell for product design.

Product detection and hole location detection is based on image recognition and checks the position of the product based on the edges and the location and pattern of the holes based on the contours of the holes. Based on AI technology and image recognition, it decides whether the product is correct, identifies the coordinates of the holes and sends the commands to a collaborative robot, which selects the appropriate program for the product.

Machine vision solution testing and validation.
At the wall panel assembly workstation, it is necessary to identify the type, location and coordinates of the product to provide the collaborative robot with the necessary parameters to generate and run the screwing program. In this case, the product is a plate of a given shape with machined holes for the screws. The holes for the screws are machined according to a specific pattern, which provides the basis for the generation of the robot program. If the program for the robot is parametric, the position of the plate in relation to the robot is not always in the same place. Therefore, it is important to provide the robot controller with the coordinates of the angular position of the plate (with respect to which the screw holes are located). The following software and hardware have been used as a solution to the problem: Cognex camera Cognex In-Sight 7905C (color camera, 5 MP), Cognex In-Sight Explorer software, Optics Fujinon HF12.5HA-1S (C-mount), Optics Moritex LMC-ML-M2516UR (C-mount), lighting (LED, flood light).

Generating the robot program (python and RoboDK)
The robot program uses a Python script to create the target points, which helps to read in the coordinates of the holes from the wall panel model. This is a machine learning technique that helps speed up the programming of the robot system. This is when the pattern or locations of the holes in the panel change. Then, generating a new program for the robot is several times faster than doing it manually.
It is important to use correct coordinate systems when generating waypoints and working trajectories: robot base (workobject UR20 Base), Instrument screwdriver TCP (workobject 104-A00_prt_driver), Workobject of the application (workobject MyWorkObject).
This program allows you to read the coordinates of openings from a csv file in a RoboDK environment through Python code. These are then marked and inserted as target points in the robot program. The target points are the motion of approaching the screwing, the motion of the screwing point and the motion of moving away from the screwing. The program has been tested in a simulation environment by simulating the screwdriving path of a specific product (wall panel).


### Technological Results
*Please describe the results of testing and validating the technological solution.*

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.



### Technical Architecture
*Please describe the technical architecture (e.g, presented graphically, where the technical solution integration with the existing system can also be seen).*
- [Component 1],
- [Component 2], 
- etc... .

![backend-architecture](https://github.com/ai-robotics-estonia/_project_template_/assets/15941300/6d405b21-3454-4bd3-9de5-d4daad7ac5b7)




### User Interface 
*Please describe the details about the user interface(i.e, how does the client 'see' the technical result, whether a separate user interface was developed, command line script was developed, was it validated as an experiment, can the results be seen in ERP or are they integrated into work process)*

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.




### Future Potential of the Technical Solution

A similar system solution can be used to automate various product assembly operations and to robotize downstream operations:
-	Product fixing and positioning
-	Moving product parts to the assembly Workstation
-	Automatic generation of collaborative robot programs based on product information
-	Detect and locate a detail and generate a programme for the robot
-	Automation of screwdriving operation – robotisation

Limitations of the system:
-	The mass of the portable product is limited by the payload of the collaborative robot
-	The workspace is limited by the distance between the input and output area and the workspace of the collaborative robot.
-	It can be replaced by a collaborative robot or an industrial robot with a larger working area. The manufacturer of the collaborative robot is not important, there may be differences in the design of the communication.

The technical solution consists of the integration of different technological capabilities, with the following components: a collaborative robot, a screw-feeding device, a rapid exchange solution for instruments, a product and its fixture, and a machine vision (MV) solution for hole detection. Artificial intelligence solutions include parametric programming of the collaborative robot (cobot), machine vision (MV) for hole location detection, product detection, digital twin (DT) generation and simulation.
Potential areas: electronics, assembly operations, furniture manufacturing, small machine components, etc.


### Lessons Learned
*Please describe the lessons learned (i.e. assessment whether the technological solution actually solved the initial challenge).*

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

