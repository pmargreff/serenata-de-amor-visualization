# Do olho neles
[De olho neles](http://www.deolhoneles.com) is a simple dashboard to parse data used by serenata de amor projects into something visual.  

## Pre-requisites

For run the project you need the latest data files from serenata de amor servers. The actual links are: 
- [Current year](https://s3-sa-east-1.amazonaws.com/serenata-de-amor-data/2016-08-08-current-year.xz)
- [Last Year](https://s3-sa-east-1.amazonaws.com/serenata-de-amor-data/2016-08-08-last-year.xz)
- [Previous Year](https://s3-sa-east-1.amazonaws.com/serenata-de-amor-data/2016-08-08-previous-years.xz)

You'll need [Julia](http://julialang.org/) language to create the files in the correct format. After download Julia you need get Dataframes and JSON packages, to do that, inside Julia call:

```
Pkg.add("DataFrames")
Pkg.add("JSON")
Pkg.update()
```

I strongly recommend at least 6 GB RAM, if you have only 4 GB you'll need 4 GB on swap to run the script. 

## Installation

First you need create the data files: 

```
chmod u+x script/create_data.sh
./script/create_data.sh absolute_path_to_file1 absolute_path_to_file2 absolute_path_to_file3
```

And, finally, install the npm dependencies: 

```
npm install
```

## Run

To create localhost, inside the main dir:

```
python -m SimpleHTTPServer
```

Open ```localhost:8000``` and be happy. 

If you haven't python installed: 

```
sudo npm install http-server -g
```

And run: 


```
http-server -p 3000 --cors
```

Open ```localhost:3000``` and be happy. 



## Contribuiting

If you don't take fire, send your issue, and all will be fine. 
