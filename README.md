# LLM Foundations

The repository is created to implement the fundamentals of the LLM concepts.

## The implementations in the repository can be seen as below:
* PyTorch review: [link to notebook](/notebooks/pytorch_review.ipynb)
* Implementation of a attention mechanism
* Implementation of a transformer architecture
* Implementation of a complete GPT architecture
* Loading pretrained GPT model weights
* Using pretrained model for fine tuning
* Implementation of a basic chat UI and getting interaction with fine-tuned model

The README file will be updated towards the end of the entire implementation of the project.

Domain information was gathered from the book "Build a Large Language Model (From Scratch)" written by Sebastian Raschka.

## To install and make the development environment up and running, please follow the steps.

1. Open terminal / command prompt and go to the target folder using: `cd <project_folder>`
2. We will use a package and project manager called "uv" to install the environment.
    * Install the package "uv" using one of the commands:<br/>
        Windows: `powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"`<br/>
        Linux or macOS: `curl -LsSf https://astral.sh/uv/install.sh | sh`<br/>
        In case of any issues please visit the documentation page to see the installation steps.
            * Documentation for uv: https://docs.astral.sh/uv/getting-started/

3. We will use python 3.12.9 in the project.
    * Check for available python versions: `uv python list`<br/>
    * Install python 3.12.9: `uv python install 3.12.9`<br/>
    * Create a virtual environment using: `uv venv --python 3.12.9`

4. After the installation of "uv" and creation of venv, we will use the pyproject.toml file to install the package.
    * Activate .venv from the terminal using: `.venv\Scripts\activate`<br/>
    * To install the entire packages, run one of the below commands:<br/>
        Torch with CPU usage: `uv sync --extra cpu`<br/>
        Torch with GPU usage: `uv sync --extra cu126`<br/>
        Link for details: https://docs.astral.sh/uv/guides/integration/pytorch/#configuring-accelerators-with-environment-markers<br/>
    * To add a specific package, use: `uv add <package_name>`

5. Select the interpreter
    * Open interpreter list.<br/>
    * If you cannot see the .venv in the list, select `enter interpreter path` and select `Find`<br/>
    * Go inside `.venv\Scripts` folder<br/>
    * Select `python.exe` file
