![placeholder image](tf.png)

# Installing Terraform

## Introduction

Terraform is an open source Infrastructure as code tool made by HashiCorp. Its used to deploy infrastructure using the HashiCorp Configuration Language (HCL). It works with multiple providers including Amazon Web Services , Microsoft Azure and Google Cloud. Its easy to read and declarative , meaning you tell Terraform what you want rather than how to build it.  

I have been using it to provision Infrastructure in Azure. This is a short tutorial on how to install Terraform on Windows. This is a short guide on how to install it.   

### Step 1  
\
Download Terraform — visit https://www.terraform.io/downloads.html and pick the version you need. I am using the Windows 64 bit version.

### Step 2 
\
Create a folder called DevOps on your C: drive . Extract the downloaded file to C:\DevOps\Terraform.

### Step 3 
\
Now we need to set the System Path , this tells Windows where to find and run Terraform.

### Step 4 
\
Now we need to set the System Path , this tells Windows where to find and run Terraform.

Open a Run command (Windows Key + R ) and type sysdm.cpl this opens up System Properties. Click on the Advanced tab and then Environment Variables.

Click on Path , under the System Variables section and click Edit .

Click on New and enter C:\DevOps\Terraform. Terraform is now setup.

NOTE — You can also do this via the cmd line using the set path command.

### Step 5
\
To verify the install open cmd or PowerShell and type terraform -version


## ☁️ Cloud Outcome
\
Terraform is installed 

## Next Steps
\
Provision some infrastructure!


