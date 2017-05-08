# Rapidclipse Demo: Using localization within a Project

This demo project shows basically the handling of a file upload. We asume, that the file is a .pdf file, so we can show it inside a XdevBrowserFrame. 

##### See following detailed informations:
1. How to upload a file
2. How to handle the file as stream
3. Basic architecture
4. How to add this ".pdf" to the XdevBrowserFrame

### Get the Projekt running 
1. Clone the GIT Reporsitory or use the import function of RapiClipse
2. File -> Import -> RapidClipse -> Demo Projects -> "rapidclipse-demo-pdfupload"
3. Maybe do some Maven updates to remove project errors 
4. Start the Project
5. Choose a .pdf File to show it inside the XdebBrowserFrame or...
6. Choose a different file for an instant download

### Basic Architekture

Important is to realize how to process the file to its way to the browser.

1. The file has to be chosen (Done by XdevUpload)
2. The file must be sent to the server (Done by XdevUpload)
3. There should be someone who waits for the file on server side and is ready to process the file (Done by the Receiver)
4. The file has to be add to the XdevBrowserframe as StreamResource (Code inside the Receiver)
5. The file has to be sent back to the client (Code inside the Receiver)

### Important files

###### 'MainView'
At the MainView you will see serveral UI Elements:

1. XdevUpload
2. XdevBrowserFrame

See the MainView Constructor for most of the Code.
