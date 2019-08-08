# README

1. Download your `kaggle.json` file from `https://www.kaggle.com/YOURUSERNAME/account`

2. For each competition you want to download data from, click on (Late) Submission and accept the rules.

3. Create a `data-download` project, in team `humancoders`.

4. Send command to Floyd to download data, via CLI:

    ```bash
    floyd init humancoders/data-download
    floyd run 'mv kaggle.json ~/.kaggle/; rm -f floyd_requirements.txt; rm -f README.md; kaggle competitions download -c avazu-ctr-prediction; gunzip *.gz' # should sync up kaggle.json file, move it to .kaggle, start download
    ```

5. Add the job's output data to a new Floyd dataset

    ```bash
    floyd data add JOB_ID
    ```

    (More info on [floyd data add](https://docs.floydhub.com/commands/data/#floyd-data-add)).
