# sem-image-classification-using-CNN
Colab Notebook for SEM image classificatioin
And a pathway towards a software for Microsopy in SEM

# Dataset
- [Paper Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6111892/)
- [Dataset Link](http://doi.org/10.23728/b2share.19cc2afd23e34b92b36a1dfd0113a89f)

# Downloading Datasets to Google Drive
- Code to download any file in Google drive

```
#importing requests librery
import requests
#Download link
file_url = "https://b2share.eudat.eu/api/files/5fc88ad5-2f13-483c-8b80-a5862c91dbbb/MEMS_devices_and_electrodes.tar"	
r = requests.get(file_url, stream = True) 
#Give a name of the for your downloaded file
with open("/content/gdrive/My Drive/MEMS_devices_and_electrodes.tar", "wb") as file: 
	for block in r.iter_content(chunk_size = 1024): 
		if block: 
			file.write(block)
```
- Code to extract data

```!tar -xvf '/content/gdrive/My Drive/MEMS_devices_and_electrodes.tar' -C '/content/gdrive/My Drive/NANOML/'```
