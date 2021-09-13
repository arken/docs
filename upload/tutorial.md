# Tutorial
## Initializing a manifest

Go to the location of your data and run. (If you're running MacOS or Linux you can navigate to the folder containing your data
in your file browser/finder and by right clicking on the folder open a terminal at that location.)

```bash
ark init
```

## Stage Data to Your manifest Submission

Still within the location of your data add specific files or folders.

```bash
ark add <LOCATION>
```

### ex.

Stage the example.csv file into your Arken Submission.

```bash
ark add example.csv
```

or to stage everything within the folder containing your data.

```bash
ark add .
```

## Submit Your Data to the manifest

This will index the added data, generate a manifest file, and either add that file
to the remote git repository or generate a pull request if you don't have access
to the main repository.

```bash
ark submit <manifest-LOCATION>
```

### ex.

Submit your data to the official
curated [Core Arken manifest](https://github.com/arken/core-manifest).

```bash
ark submit https://github.com/arken/core-manifest
```

## Uploading Your Data After Your Submission Has Been Accepted

After your submission is accepted you'll receive an email notifying you the Pull Request
has been merged into the manifest. At this point you can finally run ark upload from the directory with
your data in it to upload the data to the cluster. 
```bash
ark upload https://github.com/arken/core-manifest
```
