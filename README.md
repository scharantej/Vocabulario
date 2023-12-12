 **Design for a Flask Application to Track Spanish Vocabulary**

**HTML Files**

* `index.html`: This will be the main page of the application. It will display a list of the user's Spanish vocabulary words, along with their English translations.
* `add_word.html`: This page will allow the user to add a new word to their vocabulary.
* `edit_word.html`: This page will allow the user to edit an existing word in their vocabulary.
* `delete_word.html`: This page will allow the user to delete a word from their vocabulary.

**Routes**

* `/`: This route will render the `index.html` page.
* `/add_word`: This route will render the `add_word.html` page.
* `/edit_word/<word_id>`: This route will render the `edit_word.html` page, with the specified word pre-populated in the form.
* `/delete_word/<word_id>`: This route will delete the specified word from the user's vocabulary and redirect to the `index.html` page.

**Database**

The application will use a SQLite database to store the user's Spanish vocabulary words. The database will have the following table:

* `words`: This table will store the user's Spanish vocabulary words, along with their English translations.

**Implementation**

The application can be implemented using the Flask framework. The following code shows how to implement the `/` route:

```python
@app.route('/')
def index():
    words = get_all_words()
    return render_template('index.html', words=words)
```

The `get_all_words()` function would be responsible for fetching all of the words from the database.

The application can be run using the following command:

```
flask run
```

**Testing**

The application can be tested using the following command:

```
pytest
```

The test suite should include tests for all of the routes in the application.