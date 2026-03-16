# Steganography

Steganography is basically the scientific methodology of hiding information in form of images, audio files and texts. It is often being used by people to convey secret messages. As anticipated, steganography can be used both for good and bad purposes and Criminals use steganography to communicate their secret messages publicly, ensuring that a public image may not reveal more information than what the public image presents. In this project, I intend to focus on steganography from a technical perspective and demonstrates how it can be performed using OpenStego.

## Performing Steganography Using OpenStego in my Home Lab

<mark>**Lab Objective**</mark>

This lab session demonstrates the steps involved in performing steganography using OpenStego. Upon completion of this lab, you will be able to:

*   Learn how to hide a file within an image using OpenStego.
*   Understand the importance of encryption and password protection in steganography.
*   Export hidden files in images.

<mark>**Tool**</mark>

**OpenStego** is a free and open source steganography software that allows users to hide secret messages inside digital images or audio files.

**Step 1**

*   I installed the latest version of OpenStego software (<mark>Setup-OpenStego-0.8.6.exe</mark>) on my Windows VM

**Step 2**

*   To avoid encountering errors launching the program, I installed the latest version of Java Runtime Environment (JRE) {<mark>x64 MSI Installer > jdk-17.0.17_windows-x64_bin.msi</mark>} because OpenStego requires JRE to run.

![Screenshot of Oracle Java download page with an installation wizard overlay and a browser download sidebar.](image)

### Hiding a File in OpenStego

#### Step 1

*   I created a text folder named <mark>CFDFile.txt</mark>, composed a text in the text file, and uploaded an image named <mark>Mercedes.png</mark> in <mark>png</mark> format in my document.

![Screenshot of a text editor showing the content of CFDFile.txt.](image)

```description
The text editor shows a file named CFDFile.txt with the following content:
Hello, this message is confidential.
Hallo, diese Nachricht ist vertraulich.
The second line has a red wavy underline under "diese Nachricht ist vertraulich".
The status bar at the bottom indicates: Ln 3, Col 38 | 77 characters | Plain text | 100% | Windows (CRLF) | UTF-8
```

![File Explorer window showing three files: CFDFile (Text Document), Mercedes_PNG80195 (PNG File), and Text.txt (Text Document) in the Documents folder.](image)

### Step 2

*   I accessed the OpenStego application by double clicking it on the Desktop or wherever it might have been installed.

### Step 3

*   In the OpenStego window, <mark>under Message file</mark>, I clicked the three dots (![Three dots icon](image)) icon and double-clicked <mark>CFDFile</mark>.

![Screenshot of the OpenStego application interface. A file selection dialog "Open - Select message file" is overlaid on the main window. The "Message file" selection button is highlighted with a red box. The file "CFDFile" is selected in the dialog.](image)

### Step 4

*   In the OpenStego window, <mark>under Cover file</mark>, I clicked the three dots (![three dots icon](image)) icon and double-clicked <mark>Mercedes.png</mark>

![Screenshot of OpenStego application showing the "Hide data" tab. A file selection dialog is open over the main window, with "Mercedes_PNG80195.png" selected in the Documents folder. The "Cover file" selection button in the background is highlighted with a red box.](image)

### Step 5

*   <mark>Under Output stego</mark> file, I clicked the three dots (![three dots icon](image)) icon
*   I selected Desktop, typed <mark>“Confidential.png”</mark> and clicked Open

![Screenshot of OpenStego software showing the "Save - Select output stego file" dialog box. The user is saving a file named "Confidential" in the Documents folder.](image)

**Step 6**

<mark>Under Options, I ensured that the **Encryption Algorithm AES128** is selected</mark>

![Screenshot of OpenStego software with the "Hide data" tab active. The "Encryption algorithm" dropdown is highlighted with a red box, showing "AES128" is selected. The "Output stego file" path is set to C:\Users\Michaelcyber\Documents\Confidential.bmp.](image)

**OpenStego Form Details:**

*   **Data hiding**: [x]
    *   **Hide data**: [x]
    *   **Extract data**: [ ]
*   **Digital watermarking (Beta)**: [ ]
    *   **Generate signature**: [ ]
    *   **Embed watermark**: [ ]
    *   **Verify watermark**: [ ]
*   **Message file**: C:\Users\Michaelcyber\Documents\CFDFile.txt
*   **Cover file**: C:\Users\Michaelcyber\Documents\Mercedes_PNG80195.png
*   **Output stego file**: C:\Users\Michaelcyber\Documents\Confidential.bmp
*   **Options**:
    *   **Encryption algorithm**: AES128
    *   **Password**:     
    *   **Confirm password**:

**Step 7**

*   Under Password, I typed my password
*   Under Confirm Password, I retyped my password

![Screenshot of the OpenStego application interface showing the "Hide data" tab. The "Message file" is set to "C:\Users\Michaelcyber\Documents\CFDFile.txt", the "Cover file" is "C:\Users\Michaelcyber\Documents\Mercedes_PNG80195.png", and the "Output stego file" is "C:\Users\Michaelcyber\Documents\Confidential.bmp". Under Options, the Encryption algorithm is AES128. The Password and Confirm password fields are filled with masked characters and highlighted with a red rectangle.](image)

**Step 8**

I clicked Hide Data

**Step 9**

Popped-up Message shows <mark><font color="red">**“Message Embedded into 1 cover file(s). Skipped 0 files(s)”**</font></mark>

![Screenshot of OpenStego software showing a "Success" dialog box after embedding a message into a cover file. The main window has fields for Message file (C:\Users\Michaelcyber\Documents\CFDFile.txt) and Cover file (C:\Users\Michaelcyber\Documents\Mercedes_PNG80195.png).](image)

### Stage 2: Extracting the File in OpenStego in my Home Lab

#### Step 1

*   In the left pane, under <mark>Data hiding</mark>, click <mark>Extract data</mark>.

#### Step 2

Under <mark>Input stego</mark> file, I clicked the three dots (![Three dots icon](image)) icon and I double-clicked the <mark>Confidential image</mark>

![Screenshot of the OpenStego application showing the "Extract hidden data" tab. A file selection dialog "Open - Select input stego file" is overlaid, with the file "Confidential.bmp" selected in the Documents folder. Red boxes highlight the browse button in the main window and the file selection/Open button in the dialog.](image)

**Step 3**

Under <mark>Output stego</mark> file, I clicked the three dots (![Three dots icon](image)) icon and then in the <mark>left pane</mark>, verified that the location is selected as <mark>Desktop</mark> and clicked <mark>Open</mark>.

![Screenshot of OpenStego software showing the "Extract hidden data" process. A file dialog "Select output folder for message file" is open, with the Desktop folder selected. Red boxes highlight the folder selection button in the main window, the Desktop icon and folder name in the dialog, and the Open button.](image)

**Step 4**

* Under Password, I typed my password

**Step 5**

Then I Clicked "Extract Data"

![Screenshot of the OpenStego application showing the "Extract hidden data" tab. The "Input stego file" is set to "C:\Users\Michaelcyber\Documents\Confidential.bmp" and the "Output folder for message file" is set to "C:\Users\Michaelcyber\Desktop". A password is entered in the password field, and the "Extract data" button is highlighted with a red box.](image)

**Step 6**

*   When the Success prompt appears, I clicked OK and, on the <mark><font color="purple">Desktop</font></mark>, I double-clicked <mark><font color="purple">CFDFile</font></mark> to open it and observed the hidden text.

![Screenshot of the OpenStego application showing a "Processing" progress bar dialog box over the main interface after clicking the "Extract data" button.](image)

![Screenshot of the OpenStego software interface showing a successful data extraction process. The main window displays the "Extract hidden data" tab with file paths for the input stego file (C:\Users\Michaelcyber\Documents\Confidential.bmp) and the output folder (C:\Users\Michaelcyber\Desktop). A "Success" dialog box is overlaid, stating "Message file successfully extracted from the cover file: CFDFile.txt" with an OK button.](image)

Lab Summary

In this project, I was able to conceal sensitive information within an innocuous-looking file. This experiment and the exploration of one of several features of **OpenStego** as a free and open source steganography software that allows users to hide secret messages inside digital images or audio files, equipped me with the knowledge and skills to perform steganography and understand the importance of using appropriate Cryptographic Solutions.
