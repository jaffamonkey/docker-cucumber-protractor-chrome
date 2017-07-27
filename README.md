# Epiclabs Gherkin Test Runner
Docker image to run cucumber - gherkin protractor tests using selenium and headless chrome

### Usage:

To run this image you need a **test folder** to be used as *Volume*, inside that folder you should have a **features** folder, with your **Gherkin** syntax features (see [cucumber gherkin](https://cucumber.io/docs/reference)) and inside **features**, you should have a **step_definitions** folder with you JS definitions (Using **protractor** and **chai**)

You can also specify more **protractor parameters**, like `--specs` pointing to one feature file.

Example command:

    docker run -it --volume {YOURTESTS}:/tests epiclabs/testrunner --baseUrl {URL} {otherparams}
    docker run -it --volume /home/tests:/tests epiclabs/testrunner --baseUrl https://www.google.com --specs /tests/features/searching.feature

