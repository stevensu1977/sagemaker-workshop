
# Creating a Notebook Instance

We'll start by creating an Amazon S3 bucket that may be used in certain modules of the workshop.  Next, we'll  create a SageMaker notebook instance for running the Jupyter notebooks used in this workshop.

## 1. Create a S3 Bucket

SageMaker typically uses S3 as storage for data and model artifacts.  In this step you'll create a S3 bucket for this purpose. To begin, sign into the AWS Management Console, https://console.aws.amazon.com/.

### High-Level Instructions

Use the console or AWS CLI to create an Amazon S3 bucket (see step-by-step instructions below if you are unfamiliar with this process). Keep in mind that your bucket's name must be globally unique across all regions and customers. We recommend using a name like `smworkshop-firstname-lastname`. If you get an error that your bucket name already exists, try adding additional numbers or characters until you find an unused name.

<details>
<summary><strong>Step-by-step instructions (expand for details)</strong></summary><p>

1. In the AWS Management Console, choose **Services** then select **S3** under Storage.

1. Choose **+Create Bucket**

1. Provide a globally unique name for your bucket such as `smworkshop-firstname-lastname`.

1. Select the Region you've chosen to use for this workshop from the dropdown.

1. Choose **Create** in the lower left of the dialog without selecting a bucket to copy settings from.

</p>
</details>

## 2. Launching the Notebook Instance

1. Make sure you are on the AWS Management Console home page.  As shown below, in the **Search for services** search box, type **SageMaker**.  The search result list will populate with Amazon SageMaker, which you should now click.  This will bring you to the Amazon SageMaker console homepage.

![Services in Console](./images/console-services.png)

2. In the upper-right corner of the AWS Management Console, confirm you are in the desired AWS region. Select N. Virginia, Oregon, Ohio, or Ireland (or any other region where SageMaker is available).

3. To create a new notebook instance, click the **Notebook instances** link on the left side, and click the **Create notebook instance** button in the upper right corner of the browser window.

![Notebook Instances](./images/notebook-instances.png)

4. Type smworkshop-[First Name]-[Last Name] into the **Notebook instance name** text box, and select ml.m5.xlarge for the **Notebook instance type**.

![Notebook Settings](./images/notebook-settings.png)

5. In the **Permissions and encryption** section, choose **Create a new role** in the **IAM role** drop down menu.  Leave the defaults in the pop-up modal, as shown below. Click **Create role**.

![Create IAM role](./images/role-popup.png)

6.  As shown below, go to the **Git repositories** section, click the **Repository** drop down menu, select **Clone a Git repository to this notebook instance only**, and enter the following for **Git repository URL**: `https://github.com/awslabs/amazon-sagemaker-workshop.git`

![Enter Git info](./images/git-info.png)

7. Click **Create notebook instance** at the bottom.

### 3. Accessing the Notebook Instance

1. Wait for the server status to change to **InService**. This will take several minutes, possibly up to ten but likely much less.

![Access Notebook](./images/open-notebook.png)

2. Click **Open Jupyter**. You will now see the Jupyter homepage for your notebook instance.

