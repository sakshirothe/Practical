# Practical

Practical 1: MLOps Project Template Builder
Experiment 1 · CO PC301.1 · 10 marks
1. Aim
To create a standard project folder structure for a Machine Learning project using Python, making the project organized, reusable, and easier to maintain.
2. What is MLOps?
MLOps = Machine Learning + Operations.

It combines machine learning development with software engineering practices so that ML models can be developed, tested, deployed, and maintained efficiently.

For example, if you build a model to predict house prices, MLOps helps you organize the code, manage data, track experiments, and deploy the model.
3. What is a project template builder?
A project template builder is a Python program that automatically creates the folders and files needed for an ML project instead of making them manually.
mlops_project/

data/

models/

notebooks/

src/

README.md

requirements.txt



4. Program (Python)
You can run this using VS Code or PyCharm. No external libraries are required.

from pathlib import Path

# Create the main project folder
project_name = "mlops_project"
base_dir = Path(project_name)

# Define the folder structure
folders = [
    "data/raw",
    "data/processed",
    "models",
    "notebooks",
    "src",
    "reports"
]

# Create folders
for folder in folders:
    (base_dir / folder).mkdir(parents=True, exist_ok=True)

# Create required files
files = [
    "README.md",
    "requirements.txt",
    "src/train.py",
    "src/predict.py"
]

for file in files:
    (base_dir / file).touch(exist_ok=True)

print("MLOps project template created successfully!")

# Display the structure
for path in sorted(base_dir.rglob("*")):
    print(path)




5. How to execute it
1. Open VS Code.
2. Create a file named template_builder.py.
3. Copy the above program into the file.
4. Open the terminal and run:
   
   bash     python template_builder.py
5. Check the terminal output and the newly created mlops_project folder.
6. Expected output
MLOps project template created successfully!

mlops_project/src/train.py
