# Answers

NOTE: If you run the app and then run the tests, one of them won't fail any more because running the app seeds the db! :)

- Need to seed the db in `test_artist_repository.py::test_get_all_records`
    - When the tests are run for the first time, you should see an `UndefinedTable`
    - When you run the tests for the second time, that same test fails but now with a different error
    - The bug is that we're not seeding the db before the first test

- in `test_artist_repository.py::test_get_single_record`, need to use int for id, rather than string
    - I (Lotte) found this quite hard to spot and ended up printing `artist.__dict__` to see the difference, but the learners I ran it with spotted it pretty quick!

- in `artist_repository.py`, don't provide an id when inserting into db (and update corresponding `test_artist_repository.py::test_create_record`)
    - *This is an important one to talk through* because some learners will fix the test by inserting The Beatles with id 5, rather than realising that they shouldn't be providing an id at all!
    - The proper fix is to update Artist so that id is optional but there will be knock on effects to deal with :)

- in `test_artist_repository.py::test_get_single_record`, look for ABBA not Abba
    - will probably need `pytest -vv` flag to see this
