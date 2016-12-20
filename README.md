Test data submodule for neuroanalysis package
---------------------------------------------

To download test data for use with an existing neuroanalysis clone:

    git submodule init test_data
    git submodule update test_data

To synchronize test data with the current neuroanalysis commit:
    (checking out a commit in the main repository does _not_ automatically
     update the test data repository)

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



Contents
--------

evoked_spikes/
    Recordings of spikes evoked under different conditions--vc, cc, cell-attached, etc.
evoked_spikes/vc_evoked_spikes.npz
    Single sweep (10 channels) evoking unclamped action potentials in voltage clamp.
    Axes are (channel, sample, [signal (A), command (V)])
    These data cover a wide range of qualities and conditions from clear positives and negatives
    to ambiguous and unusable cases.
    [source: Campagnola ALM 2016.09.07/1 and 2016.09.16/0]
