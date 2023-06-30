# Working-on-the-CBIS-DDSM-data-set
This project tackles one of the major problems in computer vision which is semantic segmentation, we will be perofrming 2D segmentation to detect breast abnormalities 
We will be working on the CBIS-DDSM data set that you can fin via this link : https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=22516629

You will find two folders in this repo : The data preprocessing contains all the necessary code to get your data ready to go, and the models folder contains the models that have been trained on the data as well as the ensemble learning notebook in which we apllied the voting ensemble learning technique to enhance our segmentation task.

You will first need to execute the Restructuring the data notebook to get your folder well organised abd easier to wrok with. 

This the original folder structure:


![image](https://github.com/mohamed-ben-ticha/Working-on-the-CBIS-DDSM-data-set/assets/130346080/fb4a2f8a-ff80-4d9f-87f7-6583a144541f)

And this how it looks like after we restructure it:


![image](https://github.com/mohamed-ben-ticha/Working-on-the-CBIS-DDSM-data-set/assets/130346080/eeac7570-ee32-423a-b0ed-e48013eb857a)

Then you will need to update the dcm paths in the csv data. And finally you can start exploring your data and preprocessing it. 

After you finish preprocessing the images and their corresponding masks you will need to merge the masks of the patients that possess more than one tumour by executing the merge multi tumour notebook.


![image](https://github.com/mohamed-ben-ticha/Working-on-the-CBIS-DDSM-data-set/assets/130346080/3156ff80-1f7f-465b-b888-693e7440db25)

![image](https://github.com/mohamed-ben-ticha/Working-on-the-CBIS-DDSM-data-set/assets/130346080/7a302f11-6f17-4afe-8323-56912342ea54)



After you finish with the preprocessing pipeline you can start building your models. We used two U-net models but the only difference is in the encoder of each model since we used the basic CNN encoder for the first model and a pretrained VGG16 model for the second model.

The U-net architecture:


![image](https://github.com/mohamed-ben-ticha/Working-on-the-CBIS-DDSM-data-set/assets/130346080/fc41e3eb-d9eb-4449-8176-5377594df43f)

The VGG16 architecture:


![image](https://github.com/mohamed-ben-ticha/Working-on-the-CBIS-DDSM-data-set/assets/130346080/990efea7-ddd2-4c21-8ebf-1bffe004f5e4)


