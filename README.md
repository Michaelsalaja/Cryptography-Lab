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

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%201.png)
Figure 1

### Hiding a File in OpenStego

#### Step 1

*   I created a text folder named <mark>CFDFile.txt</mark>, composed a text in the text file, and uploaded an image named <mark>Mercedes.png</mark> in <mark>png</mark> format in my document.

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%202.png)
Figure 2

```description
The text editor shows a file named CFDFile.txt with the following content:
Hello, this message is confidential.
Hallo, diese Nachricht ist vertraulich.
The second line has a red wavy underline under "diese Nachricht ist vertraulich".
The status bar at the bottom indicates: Ln 3, Col 38 | 77 characters | Plain text | 100% | Windows (CRLF) | UTF-8
```

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%203.png)
Figure 3

### Step 2

*   I accessed the OpenStego application by double clicking it on the Desktop or wherever it might have been installed.

### Step 3

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%204.png)
Figure 4


### Step 4

*   In the OpenStego window, <mark>under Cover file</mark>, I clicked the three dots (![three dots icon](image)) icon and double-clicked <mark>Mercedes.png</mark>

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%205.png)
Figure 5

### Step 5

*   <mark>Under Output stego</mark> file, I clicked the three dots (![three dots icon](image)) icon
*   I selected Desktop, typed <mark>“Confidential.png”</mark> and clicked Open

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%206.png)
Figure 6

**Step 6**

<mark>Under Options, I ensured that the **Encryption Algorithm AES128** is selected</mark>

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%207.png)
Figure 7

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

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%208.png)
Figure 8

**Step 8**

I clicked Hide Data

**Step 9**

Popped-up Message shows <mark><font color="red">**“Message Embedded into 1 cover file(s). Skipped 0 files(s)”**</font></mark>

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%209.png)
Figure 9

### Stage 2: Extracting the File in OpenStego in my Home Lab

#### Step 1

*   In the left pane, under <mark>Data hiding</mark>, click <mark>Extract data</mark>.

#### Step 2

Under <mark>Input stego</mark> file, I clicked the three dots (![Three dots icon](image)) icon and I double-clicked the <mark>Confidential image</mark>

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%2010.png)
Figure 10

**Step 3**

Under <mark>Output stego</mark> file, I clicked the three dots (![Three dots icon](image)) icon and then in the <mark>left pane</mark>, verified that the location is selected as <mark>Desktop</mark> and clicked <mark>Open</mark>.

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%2011.png)

**Step 4**

* Under Password, I typed my password

**Step 5**

Then I Clicked "Extract Data"

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/598f5ac9fb43ba2e3f483aa110056a7e4dcad87a/Figure%2015.png)


**Step 6**

*   When the Success prompt appears, I clicked OK and, on the <mark><font color="purple">Desktop</font></mark>, I double-clicked <mark><font color="purple">CFDFile</font></mark> to open it and observed the hidden text.

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%2013.png)

![image alt](https://github.com/Michaelsalaja/Cryptography-Lab/blob/fb28b06e9c3e79f627a74883fe8a8434dc02639e/Figure%2014.png)

Lab Summary

In this project, I was able to conceal sensitive information within an innocuous-looking file. This experiment and the exploration of one of several features of **OpenStego** as a free and open source steganography software that allows users to hide secret messages inside digital images or audio files, equipped me with the knowledge and skills to perform steganography and understand the importance of using appropriate Cryptographic Solutions.
