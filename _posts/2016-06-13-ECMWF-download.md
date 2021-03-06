---
layout: post
title: Installing Python Library for downloading ERA-Interim Data
---

### Update: The ECMWF api client is now available on pypi.  
Installation (step 1-3) can be done by the command:
> pip install ecmwf-api-client

### Old steps (1-3)

```
(1) Installing the package requires the python Setuptools. You can set it up locally with the command:

> wget https://bootstrap.pypa.io/ez_setup.py -O - | python - --user

(2) Download the Python library package and unzip it (You can do it in any directory)
> wget https://software.ecmwf.int/wiki/download/attachments/56664858/ecmwf-api-client-python.tgz
> tar zxf ecmwf-api-client-python.tgz

You shall see four items extracted:
- example.py
- ecmwfapi/__init__.py
- ecmwfapi/api.py
- setup.py

(3) In the directory with these four items, install the package with:
> python setup.py install --user
```

(4) To use the sample script, you need an API key ( .ecmwfapirc ) placed in your home directory. You can retrieve that by logging in: https://api.ecmwf.int/v1/key/
Create a file named ".ecmwfapirc" in your home directory and put in the content shown on the page:

```
{
    "url"   : "https://api.ecmwf.int/v1",
    "key"   : "(...)",
    "email" : "(...)"
}
```

(5) After doing that, in the directory with the sample script example.py, you can test the package by running it:
> python example.py  

You should see it successfully retrieves a .grib file if the package has been set up properly.

(6) To download python script for retrieving ERA-Interim netCDF files, there are sample script available here (look under "Same request NetCDF format"):
[https://software.ecmwf.int/wiki/display/WEBAPI/Python+ERA-interim+examples]

In fact, on the ECMWF Public Dataset web interface page you retrieve ERA-Interim data, after you select the subset of data, instead of pressing "Retrieve NetCDF", there is another button named "View the MARS request", and it will show how the python script for retrieving that dataset looks like.

I learnt the above steps on these pages:
- [ECMWF python library](https://software.ecmwf.int/wiki/display/WEBAPI/Access+ECMWF+Public+Datasets#AccessECMWFPublicDatasets-python)
- [Python setuptool](https://pypi.python.org/pypi/setuptools)
