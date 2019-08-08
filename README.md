# README

1. Download your `kaggle.json` file from `https://www.kaggle.com/YOURUSERNAME/account`

2. For each competition you want to download data from, click on (Late) Submission and accept the rules.

3. Create a `data-download` project on Floyd, in team `humancoders`.

4. Send command to Floyd to download data, via CLI:

    ```bash
    floyd init humancoders/data-download
    floyd run --task house-prices
    ```

5. Add the job's output data to a Floyd dataset. This can be done from the Job's webpage or via [floyd data add](https://docs.floydhub.com/commands/data/#floyd-data-add)).
