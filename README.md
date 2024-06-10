# Getting Started with Django on Linux

A guide for getting started with Django by creating a Django project, a Django app, making the initial migration, and running the Django development server.

## 1. Getting Started

### A. Resources

For a more comprehensive guide to working with [Django](https://www.djangoproject.com/), check out the official [Django documentation](https://docs.djangoproject.com/en/5.0/).

### B. Requirements

For the purposes of this guide, you will need:

- A [Linux](https://www.linux.org/pages/download/) operating system.
- [Python](https://www.python.org/) version 3 or higher installed in your system.
- A [code editor](https://www.codecademy.com/resources/blog/popular-ides-and-code-editors/) e.g. [VSCode](https://code.visualstudio.com/).

## 2. Initializing Django

Before you can install Django and create a Django project or app, you will need to set up a **virtual environment**.

### A. Virtual Environment

Think of a **virtual environment** as a container to store all the packages/libraries that you will use in your Django project.

- This sets aside your project's packages from those already installed globally in your system.
- It also helps you avoid overloading your project with the other installed packages, which you may not need/want to use in the project.

Learn more about a **Python virtual environment** in the official [Python documentation](https://docs.python.org/3/library/venv.html).

#### i. Create a virtual environment

In your code editor's workspace, take the following steps to create a virtual environment:

- Open your terminal and run the following command:

  ```
  virtualenv venv
  ```

  ![image](https://github.com/benie254/django-getting-started/assets/99865051/4bd3cec8-d3ad-420b-8467-5648daad20cf)

- Let's break down the command:
  - `virtualenv` is the section of the command that triggers the creation of the virtual environment.
  - `venv` is the (conventional) name of your virtual environment. You may name it anything relevant like `env` or whatever you'll prefer.
- If you're following this guide step-by-step, you will notice a new folder titled `venv` created in the root directory of your workspace.

  ![image](https://github.com/benie254/django-getting-started/assets/99865051/59f7df33-ab51-46af-953e-efefbad26a85)

#### ii. Activate your virtual environment

After creating a virtual environment, you need to activate it before you can use it to store libraries/packages that you will install.

- Run the following command to activate your virtual environment:
  ```
  source venv/bin/activate
  ```
- You may replace `venv` with the name you used when creating your virtual environment.

### B. `gitignore`

Before you can proceed with installing Django, you need to do one more thing: put the `gitignore` file to use.

A gitignore file stores all folders and files that you do not want to be pushed to your remote GitHub repository.

You should keep the size of your remote repository as light as possible, and push only what is necessary to it.

You should also keep sensitive information/data in your local system and not expose them to the public by pushing them to GitHub. A `gitignore` file comes handy in this case as well.

You will add your virtual environment to `gitignore`. Later on, you will learn how to retrieve the packages/libraries stored in your virtual environment so that you can still access these `dependencies` even when you don't have access to the virtual environment that you created earlier on.
