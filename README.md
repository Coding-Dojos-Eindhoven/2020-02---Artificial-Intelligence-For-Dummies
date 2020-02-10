Artificial Intelligence (For Dummies): Q-Learning
=================================================

Preparation Instructions
------------------------

This coding dojo uses Python, version 2.7 to be precise. If you're experienced
using Python and you have a working Python 2.7 setup configured, please feel
free to use that. Otherwise, you can follow theses instructions to prepare for
the coding dojo, so that we can get started right away.

- Install [Miniconda][Miniconda]. On macOS you can also use homebrew if you have
  that installed: `brew cask install miniconda`. Verify that it works and is up
  to date. You can do that in a terminal by running:

  ```bash
  $ conda update -y conda
  [... lots of output ...]
  Preparing transaction: done
  Verifying transaction: done
  Executing transaction: done
  $ conda --version
  conda 4.8.2
  $ conda init <your shell, eg zsh or bash>
  [...]
  modified      /Users/nlv19703/.zshrc
  [...]
  ```

- Close the terminal and open a new one for the changes to take effect.
- Clone the repository that we will be using for the coding dojo: `git clone
  https://github.com/Mocolate/reinforcement_learning_pacman.git`.

These setup instructions assume that you'll be using [PyCharm Community
Edition][PycharmCE]. (If you want to use something else, make sure you know how
to get everything up and running using that IDE/Editor.) After installing
Pycharm, follow these steps:

- In the Welcome screen, choose 'Create New Project'.
- Pick a folder where you want to store the project, and a new folder named
  `qlearning` inside that folder.
- Expand the "Project Interpreter: New Conda environment" settings.
- Make sure "New environment using: Conda" is selected.
- Change the Pyton version to 2.7.
- Click "Create".
- PyCharm will create the Conda environment; this may take a while.
- In the steps above, you cloned a repo. It has a folder `reinforcement`. Copy
  all files and folders inside of that to the new project folder you just
  created. So there should now (amongst others) be a file `requirements.txt`
  inside your `qlearning` folder.
- Open a terminal inside PyCharm. This should cause the conda environment to be
  automatically activated inside that terminal. If you're not sure: `conda info`
  should say that the active environment is `qlearning`. (If it's not active,
  run `conda activate qlearning`.)
- Run the following command to install the dependencies:

  ```bash
  $ pip install -r requirements.txt
  [...]
  Successfully installed atomicwrites-1.3.0 attrs-19.3.0 configparser-4.0.2 contextlib2-0.6.0.post1 funcsigs-1.0.2 importlib-metadata-1.5.0 more-itertools-5.0.0 packaging-20.1 pathlib2-2.3.5 pluggy-0.13.1 py-1.8.1 pyparsing-2.4.6 pytest-4.6.9 scandir-1.10.0 six-1.14.0 wcwidth-0.1.8 zipp-1.1.0
  ```

- Verify if your setup if fully functional by running:

  ```bash
  $ pytest tests/test_if_it_works.py
  [...]
  ========================= 1 passed in 0.03s =========================
  ```

  If you get errors at this point, you should verify that you are using the
  correct version of `python` and `pytest`. In the output of `pytest` you can
  see both. If this is incorrect, run `which pytest` to see which one you are
  using. It should be the one inside the conda `qlearning` env; if not, run
  `rehash` or open a new terminal and try again. If that still fails, make sure
  that conda comes first in your path.

[Miniconda]: https://docs.conda.io/en/latest/miniconda.html
[pycharmCE]: https://www.jetbrains.com/pycharm/download
