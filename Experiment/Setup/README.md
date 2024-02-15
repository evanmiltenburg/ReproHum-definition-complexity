# How to set up the experiment in Qualtrics

Start a blank survey from scratch:
1. Click "Create a new project"

2. You will see a header titled "From scratch" with a button to create a survey. Click that button, and then click the "Get Started" button that appears.

3. You will see a text field and a dropdown menu.
    a. Choose any name that you like.
    b. For "How do you want to start your survey?", select "Create a blank survey project." (Do not select the option to create a survey using QSF. The advanced question format that we are using is different from QSF, in that QSF files are in a proprietary JSON format and we are using the more limited specification format.)

4. Under the "Survey" tab (the default view), click the "Tools" button and click on "Import/Export>Import survey".

5. You will be asked to choose a file. Navigate to the `Questions/` folder and select the `all_questions.txt` that was generated using the notebook. Upload it. This will take a while because Qualtrics is a bit slow to process relatively large questionnaires. (After all, we have 300+ questions.)

6. Delete the default question block in Qualtrics. (Click the three dots '...' in the upper right corner, and look for the delete option in the context menu.) This block was automatically added by Qualtrics to have a place to put your questions, but we are not using it.

7. Now we are ready to specify the survey flow. There is a small button on the top left of your screen that will take you to the survey flow environment.

8. Use the option to add new elements (`+ Add new element here`). There will be a menu asking you what you want to add.
    a. Click on `Branch` to add branching logic to the survey. You still need to specify a condition.
    b. Click on `Add a condition` to specify the flow. Select the question "What set of items would you like to work on?" and specify the answer "1".
    c. Now move Block 2 (the first block with items-to-be-rated) by dragging it on top of the branching logic. If successful, you will see that this block is now indented, so it will only be shown to participants who specified the answer "1".
    d. Repeat the same procedure for all ten lists. Block 3 will be shown if answer "2" is selected, Block 4 will be shown if answer "3" is selected, and so on until all ten lists of items are covered by the branching logic.

9. Now it is time to add forced response requirement. For each block of questions:
    a. Select the first question.
    b. Shift-click the last question to select all 30 questions.
    c. Click "Add requirements". Force response should be on by default.