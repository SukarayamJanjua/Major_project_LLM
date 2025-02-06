# **SMART-LLM: Cognitive Bot using Large Language Models**

Shriram, Aashan, Abhishank, Sukarayam, Aviral 

Major project under supervision of Dr. Ravi Verma, NITJ


**Abstract:** Multi-robot systems are emerging in a wide variety of applications such as household automation and search-and-rescue missions. But the complexities of task allocation in such heterogeneous systems really challenge the whole enterprise. 
This project proposes a novel framework for using Large Language Models (LLMs) to optimize multi-robot task planning. It converts natural language instructions into structured task plans for robots.
It uses Large Language Models (LLMs) like GPT-4 to plan and allocate tasks.


## Setup
Create a conda environment (or virtualenv):
```
conda create -n smartllm python==3.9
```

Install dependencies:
```
pip install -r requirments.txt
```

## Creating OpenAI API Key
The code relies on OpenAI API. Create an API Key at https://platform.openai.com/.

Create a file named ```api_key.txt``` in the root folder of the project and paste your OpenAI Key in the file. 

## Running Script
Run the following command to generate output execuate python scripts to perform the tasks in the given AI2Thor floor plans. 

Refer to https://ai2thor.allenai.org/demo for the layout of various AI2Thor floor plans.
```
python3 scripts/run_llm.py --floor-plan {floor_plan_no}
```
Note: Refer to the script for running it on different versions of GPT models and changing the test dataset. 

The above script should generate the executable code and store it in the ```logs``` folder.


Run the following script to execute the above generated scripts and execute it in an AI2THOR environment. 

The script requires command which needs to be executed as parameter. ```command``` needs to be the folder name in the ```logs``` folder where the executable plans generated are stored. 
```
python3 scripts/execute_plan.py --command {command}
```
## Dataset
The repository contains numerous commands and robots with various skill sets to perform heterogenous robot tasks. 

Refer to ```data\final_test\``` for the various tasks, robots available for the tasks, and the final state of the environment after the task for evaluation. 

The file name corresponds to the AI2THOR floor plans where the task will be executed. 

Refer to ```resources\robots.py``` for the list of robots used in the final test and the skills possessed by each robot. 



