# Jarvis

[![Build Status](https://travis-ci.org/sukeesh/Jarvis.svg?branch=master)](https://travis-ci.org/sukeesh/Jarvis)

A Personal Assistant for Linux and MacOS

![Jarvis](http://i.imgur.com/xZ8x9ES.jpg)

Jarvis is a simple personal assistant for Linux and MacOS which works on terminal. He can talk to you if you enable his voice. He can tell you the weather, he can find restaurants and and other places near you. He can do some great stuff for you. Stay updated about [new functionalities](NEW_FUNCTIONALITIES.md).

## Getting Started

In order to start Jarvis just clone the repository and run the command: `python jarviscli`.

You can start by typing `help` within the Jarvis command line to check what Jarvis can do for you.

### Prerequisites

Use the command `./setup.sh` to install the requirements.

## Youtube Video

[Click here](https://www.youtube.com/watch?v=PR-nxqmG3V8)

## Contributing

- PR's are accepted!!
- We follow PEP 8 guidelines. Before making a PR, make sure that your code is according to PEP8 standards.
- If you have some ideas for new features and you don't have time to implement them please open an issue with the tag new_feature
- If you have time to add extra functionality to Jarvis (for example new actions like "record" etc.) you only need to add this action to the actions tuple (look on init(self) in CmdInterpreter.py) as a string if it's a one word command or as a dict if it's a two word command. Then, add **appropriate methods** (substitute `record` for the name of your command):
  + `do_record(self, s)`: implement here your command functionality. `s` is where Jarvis will pass the arguments of your command.
  + `help_record(self)`: print what your command does.
  + **(optional)** `complete_record(self)`: useful to get completions, if it's a two word command use `get_completions` method:
    + `return self.get_completions("record", text)`
- Please don't forget to comment (document) your code

**Note**: one word command examples are: `say [text that Jarvis will speak]`, `weather`. Two word command examples are: `hotspot start`, `hotspot stop`, `increase volume`, `decrease volume`.

 ### How to run tests:
 **For PEP8**
 
 Change into Jarvis directory
 ```bash
 cd Jarvis
 ```
 Then run coala
 ```bash
 coala --ci
 ```
**For tests**

 Add `__init__.py` file in jarviscli/tests/test_manual/
 
 Change into the Jarvis/jarviscli directory
 ```bash
 cd Jarvis/jarviscli
 ```
 Then run unittest discover
 ```python
 python -m unittest discover
 ```

## Authors

 **sukeesh**

See also the list of [contributors](contributors.md) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details
