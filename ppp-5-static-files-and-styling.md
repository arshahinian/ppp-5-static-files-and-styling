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
* Once you've successfully implemented the above two pages, this is what your app may look like.
## Learn About Static Files
* While it's great we've added more functionality, our app still looks quite bland.
* We should probably add some styling.
* To do so, technically we could use the <style type="text/css"> tag in the head of our HTML file.
* However, you can imagine how that could get unruly, especially if we created more views.
* If we did that, we'd have to copy and paste the entire style tag and its CSS rules into each individual file.
* Not only is that not DRY, it would mean that any time we want to make a change to the CSS, we would have to make that change in every single file.
* Not very fun or efficient.
* Luckily, we can avoid that by using static files.
* Read through this section on static files in the Flask docs to learn about them.
### Static Files
* Dynamic web applications also need static files.
* That’s usually where the CSS and JavaScript files are coming from.
* Ideally your web server is configured to serve them for you, but during development Flask can do that as well.
* Just create a folder called static in your package or next to your module and it will be available at /static on the application.
* To generate URLs for static files, use the special 'static' endpoint name: url_for('static', filename='style.css')
* * The file has to be stored on the filesystem as static/style.css.
## Using Static Files
* Once you've learned about static files, try creating your own to add styling.
### Create a style.css file
1. Create a static folder within the petfax folder.
2. In that folder, create a style.css file.
3. Add a simple CSS rule in the file, like adding a background color to the body.
4. In all your HTML templates, link your style.css using the static file syntax you just learned about.
* Note: You may need to restart your Flask server for the changes to take effect.
5. Once you've successfully linked your file, have fun with some styling!
* Feel free to style as much or as little as you want.
### Style inspiration
* Want some style inspiration? Here's one example.
* If you would like to use this styling, take a look at the CSS and HTML in the part4 branch of the repository.