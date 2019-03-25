# Tutorial: Captioning every image in a folder

Runway makes it really simple to use AI to process your own photo albums, media libraries, and documents. This tutorial will guide you through generating captions for every image in a folder using the model im2txt and Runway's "Export to File" functionality.

![still images](https://runway.nyc3.cdn.digitaloceanspaces.com/documentation/tutorial_im2txt_medialibrary/0_dataset.png)

### Step 1

In this tutorial, we will use **im2txt**, which is based on the paper [Show and Tell: A Neural Image Caption Generator](https://arxiv.org/pdf/1411.4555.pdf) released by Google Research. The first step is selecting the im2txt model from the Model Directory.

![step 1](https://runway.nyc3.digitaloceanspaces.com/documentation/0.2.0/im2txt01.jpg)

### Step 2

In this view, you can view information about the model, including a description of what the model does, licensing information, as well as the model input and output datatypes (`image` for the input image and `array[text, number]` for a list of captions and probabilities for each generated caption). To use im2txt, you will first need to add the model to a workspace. 

![step 2](https://runway.nyc3.digitaloceanspaces.com/documentation/0.2.0/im2txt02.jpg)


### Step 3 

If you haven't installed **im2txt**, the bottom right button will prompt you to install the model.  **You need to have Docker installed in order to continue.**

![step 3](https://runway.nyc3.digitaloceanspaces.com/documentation/0.2.0/im2txt03.jpg)


?> Some deep learning models might be large so please note that downloading the model might take a couple of minutes. In this case, AttnGAN might take **4 to 8 minutes** to download depending on your internet connection.

![step 3](https://runway.nyc3.digitaloceanspaces.com/documentation/0.2.0/im2txt04.jpg)


### Step 4

Once the model has been installed we are ready to select the input and output for the model. For the input, that is the folder of images that we want to caption. First, select "File" from the Input Type dropdown.

![step 4](https://runway.nyc3.cdn.digitaloceanspaces.com/documentation/tutorial_im2txt_medialibrary/6_select_file_input.png)

### Step 5

Click "Import" and find the folder that you want to caption from your local filesystem.

![step 5](https://runway.nyc3.cdn.digitaloceanspaces.com/documentation/tutorial_im2txt_medialibrary/7_click_import.png)
![select folder](https://runway.nyc3.cdn.digitaloceanspaces.com/documentation/tutorial_im2txt_medialibrary/8_select_folder.png)

### Step 6

Now that we have imported our image folder into Runway, it's time to specify where how we want to store the captions generated by the model. First, select "File" from the Output Type dropdown. By default, the captions are saved in a tabular CSV format, where every row contains the image filename that we are captioning along with the im2txt model's predicted captions. We use CSV for this tutorial -- JSON is also supported.

![step 6](https://runway.nyc3.cdn.digitaloceanspaces.com/documentation/tutorial_im2txt_medialibrary/9_select_file_output.png)

<p class="note"><b>NOTE:</b> Exports are stored by default in the following folders depending on your operating system: <code>\Users\USERNAME\Downloads</code> for Windows, <code>/Users/USERNAME/Downloads</code> for Mac, and <code>/home/USERNAME/Downloads</code> for Linux. You can change the destination path for your exports via the app's settings.

</p>

### Step 7

We have selected our input folder, and our output destination, so we can finally run the model to process our images. Click "Run im2txt" and wait for a few seconds for the model to start.

![step 7](https://runway.nyc3.cdn.digitaloceanspaces.com/documentation/tutorial_im2txt_medialibrary/10_run_model.png)

### Step 8

Once the model has started running, the "Start Exporting" button will become active. Click the button to start processing your images one by one.

![step 8](https://runway.nyc3.cdn.digitaloceanspaces.com/documentation/tutorial_im2txt_medialibrary/11_start_exporting.png)

### Step 9

Wait while the model processes each of your images individually...

![step 9](https://runway.nyc3.cdn.digitaloceanspaces.com/documentation/tutorial_im2txt_medialibrary/12_export_in_progress.png)

### Step 10

Once the export has been completed, you will see a notification on the bottom of the app. Click the notification to navigate to the folder where the resulting CSV file has been saved.

![step 10](https://runway.nyc3.cdn.digitaloceanspaces.com/documentation/tutorial_im2txt_medialibrary/13_export_completed.png)

### Step 11

Open the CSV file to view all the captions predicted by the model!

![step 11](https://runway.nyc3.cdn.digitaloceanspaces.com/documentation/tutorial_im2txt_medialibrary/14_csv_result.png)

### Summary

This tutorial shows how to use an image captioning model, called im2txt, to generate captions for every image in a folder. You can use the same approach for other predictive models inside Runway.