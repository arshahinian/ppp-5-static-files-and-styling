* https://digitalskills.instructure.com/courses/4913/pages/activity-ppp-5-static-files-and-styling?module_item_id=642846
* Activity (ppp-5-static-files-and-styling)
# Activity: Static Files and Styling
* In this activity, we will add some more polish to PetFax by adding styling and a few more pages.
* In addition, you will do some self-learning with Flask about how to use static files.
## Getting Started
1. Open your terminal.
2. Navigate to where you cloned the PY-petfax-app repository.
3. Open it in your code editor of choice.
4. Activate the virtual environment by running . venv/bin/activate in the root of the repository.
5. Run the app with flask run --reload.
## Adding New Routes
* So far, we only have an index page that displays all the pets available for adoption.
* While that's great, we could certainly add more functionality.
* In this section, we'll add:
* * A show page for each individual pet.
* * * This is where we'll display the fun facts that accompany each one.
* A create page for facts.
* * The shelter has asked us to include a form that will allow guests to submit fun facts for possible future use-this is where that will go.
* * * For now we'll just serve the page and form, and handle the actual form submission in a later lesson.
* It's up to you to add the above two pages!
* * However, here are some hints that may help.
### Hints for the pet show page
* Your show page endpoint should follow the typical RESTful routing pattern (i.e., /pets/<index>).
* * Read the variable rules section in the docs for a refresher about adding variables to routes.
* Recall that the given data are provided as a list of objects.
* * However, for this route, you only need to pass the show page information about one particular pet.
* * * Can you recall how to select a specific element in a list using its index?
* On the index page, be sure to add links for each adoptable pet that would take the user to the show page.
* * How would you dynamically create the list?
* * * Consider looking at the given data and see if there's any way you can get its index that way.
* On the show page itself, display the pet's name, image, and the provided fun fact.
### Hints for the facts create page
* Consider: would /pets/new make sense as an endpoint for this page?
* * Or should a new blueprint for facts be created instead?
* Don't worry about making the form POST work, just make it so that going to /facts/new displays a form.
* For the form, include an input for submitter, which would be the submitter's name.
* * Also include a text area for the fact itself.
* * * Make sure to include some way to submit the form.
#### Expected functionality
* See image file:
* * lessons-ppp-5-static-files-and-styling-Activity.2.png


