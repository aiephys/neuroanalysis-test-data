Test data submodule for neuroanalysis package
---------------------------------------------

To download test data for use with an existing neuroanalysis clone:

    git submodule init test_data
    git submodule update test_data

To add new test data:

    # First update the test data repository:
    cd test_data
    git commit ...
    git push
    cd ..

    # Next update the main repository to refer to the latest test_data commit:
    git commit test_data
    git push

