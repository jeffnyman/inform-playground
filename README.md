# Inform Playground

_Simplified Distribution of the Inform System_

This repository sets up a simplified distribution of [Inform 7](https://ganelson.github.io/inform-website/) ([repo](https://github.com/ganelson/inform/tree/master)).

# Usage

Set up your environment `PATH` so that it looks for the relevant `inform7` binary in this distribution.

To test out the execution, perform the following steps:

* Create a `projects` directory in the playground directory.
* Create a `testing.i7`` file in that directory.
* Run the following: `inform7 -internal ./Internal -basic projects/testing.i7`

This should generate a `testing.i6` file. Now you can do this:

* `inform6 -G projects/testing.i6`

You can also generate an Index:

* `inform7 -internal ./Internal -basic projects/testing.i7 -index`

You can also create a full project.

* Create a `Testing.inform` directory in the projects directory.
* Create a `Source` directory within that and create a `story.ni` file within that.
* Make sure there is a `uuid.txt` file in the main directory.
* Run the following: `inform7 -internal ./Internal -project projects/Testing.inform -basic -index`

To try a full compile of the project that is generated:

* `inform6 -wSDG +include_path=projects/Testing.inform/Source,. projects/Testing.inform/Build/auto.inf projects/Testing.inform/Build/output.ulx`
