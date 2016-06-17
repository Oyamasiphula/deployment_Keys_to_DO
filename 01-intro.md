---
layout: default
title: Welcome yourself to the Cloud-Computing.
---

# 1.Concepts briefing & The Basic flow of Digital Ocean's sequence

Cloud computing is the practice of using a network of remote servers hosted on the Internet to store, manage, and process data, rather than a local server or a personal computer.

![image-title-here](/img/posts_Schematics/cloud-computing-gears.jpg){:class="img-responsive"}

# Introduction

DigitalOcean calls its virtual private servers Droplets; each Droplet that you sign up is a new VPS for your personal use.

<h3>  About Virtual Private Server</h3>
A virtual private server (VPS) is a virtual machine sold as a service by an Internet hosting service. A VPS runs its own copy of an operating system, and customers have superuser-level access to that operating system instance, so they can install almost any software that runs on that OS.

Note. You will be receiving email notifications from Digital Ocean.

NB.`The First email notification you will receive it is going to be your account credentials for that specific (droplet) you've just created.`

<h3>continuation ...  </h3>

* Now you don't have to worry about logging in again you are now permanently authorised.

# How To Create Your First DigitalOcean Droplet Virtual Server

<h3>Step One — Signed in and you want to Create Droplet</h3>
![image-title-here](/img/posts_Schematics/welcomepagetocreatedroplet.png){:class="img-responsive"}

<p><code>01</code>.To create your first Droplet go to the DigitalOcean Control Panel and log in with your email and password. The create button will be right there on the first page: click on "Create Droplet".</p>
<br />
<h3> Step Two — Select Droplet Image </h3>
<p>You can create your Droplet image from 4 possible categories</p>

* `02`.`As a begginer we would recommended you to chose UBUNTU image ["CLOUD SERVER OPERATING SYSTEM"] and at this stage you should at least know how UBUNTU TERMINAL WORKS just for the future purpose which is when you are done creating your droplet.`

![image-title-here](/img/posts_Schematics/osimages.png){:class="img-responsive"}

<h3> Distributions </h3><p>Create from several operating systems, such as Ubuntu, Debian, CoreOS, and CentOS. After selecting your distribution, be sure to select the image of your choice (specifying the version and 64 bit or 32 bit).</p>

<h3> One-click Apps </h3>
<p>Create from images that have pre-installed and configured programs that will get your Droplet off to a strong start.</p>

<h3> Snapshots: </h3>
<p>Create from a snapshot that you previously made, letting you create backup copies or scale quickly.</p>

<h3> Backups </h3>
<p>Create from a previously automatically generated backup, the option that you can enable on each Droplet individually with the "Backups" button.</p>

<h3> 32-bit vs. 64-bit Systems </h3>
<p>A 32-bit operating system is recommended for cloud servers with less than 3 GB of RAM -- this is especially true for servers with 1 GB, or less, of RAM. Processes can require significantly more memory on the 64-bit architecture. On servers with a limited amount of RAM, any performance benefits that one might gain from a 64-bit operating system would be diluted by having less memory available for buffers and caching.</p>
<br />
<h3>Step Three-Select Your Droplet's Size depending on your needs and budget, you can select the Droplet option that works best for you.</h3>

<p><code>03</code>.You should chose the cheapest image with less space which is going to be 20GB and each project isn't going to even exceed 100MegaBytes, otherwise you can upgrade your droplet. You could get your droplet up and running again without losing your stuff hence all files are safe only when a backup is created.</p>

![image-title-here](/img/posts_Schematics/imagesizes.png){:class="img-responsive"}

<p>There is a wide spectrum for prices, power, and storage capacity. The smallest and least expensive option starts at 512MB of RAM with 1 CPU and 20GB of SSD storage. The size options grow larger from there, all the way up to 64GB of RAM with 20 CPUs and 640GB of SSD storage. Should your needs change at a future point, you can adjust your Droplet's plan using the flexible and permanent resize options.</p>

<br />
<h3>Step Four - Select Your Droplet Region</h3>

<p>You may choose the most effective region for your Droplet location. Although equally powerful, the best region to choose is the one nearest to you and your customers or other possible users. Selecting a more distant server location may increase your server latency without serving any practical purpose.</p>

![image-title-here](/img/posts_Schematics/dropletregion.png){:class="img-responsive"}

`04`.Then for this you need to know which region is the closest from your current region then for a our case we are currently in South Africa.Therefore on our case :us: `New York` is going be our best `datacenter` option to choose.

<br />
<h3>Step Five — Select Additional Options</h3>
The Select additional options section allows you to select which features you would like your Droplet to have:

![image-title-here](/img/posts_Schematics/additionalOpt.png){:class="img-responsive"}

* `Private Networking`: Enables a private networking interface, in addition to the default public interface, that can only be accessed via the private network of other Droplets within the same datacenter.

* `Backups`: Enables automatic backups of the Droplet — for more information about the backup service,click on the following link:
https://www.digitalocean.com/community/tutorials/digitalocean-backups-and-snapshots-explained

* `IPv6`: Enables IPv6 access for your Droplet.

* `User Data`: Enables you to pass arbitrary data into the user-data key of the DigitalOcean Metadata service. This setting is required for CoreOS Droplets. To read more about user data, check out the tutorial on Droplet Metadata.

Select any of the settings you would like to enable. The Private Networking feature is very useful if you have multiple Droplets in the same datacenter that communicate with each other.

`The following instruction is for later you can skip this part to step 7.`

<br />
<h3>Step Six — Select SSH Keys (Optional)</h3>
`Optional`: Select which SSH keys you would like to add to your new Droplet.

![image-title-here](/img/posts_Schematics/extraOption.png){:class="img-responsive"}

<p>It is recommended that you set up SSH keys to authenticate to your Droplets because it provides better security than a basic password. For more information about setting up SSH keys with your DigitalOcean Droplets, refer to this tutorial.</p>

<br />
<h3>Step Seven — Select the Number and Names of the Droplets to Create</h3>

<p>Next, you can choose the number and names of the Droplets you wish to create. Depending on the number of Droplets currently in your account, you can create up to five Droplets that will use the configuration that you have selected. By default, a single Droplet is set to be created. You can adjust the number of Droplets to create be clicking the plus or minus buttons.</p>

<p>Each Droplet must have a name. This name will be used in the DigitalOcean control panel and as the server's hostname. A default name will be provided for your Droplet(s) based on the options you have selected, but you can modify the name(s) to best suit your needs. You may want to use a Fully Qualified Domain Name (e.g. droplet1.example.com).</p>

![image-title-here](/img/posts_Schematics/finalizeandcreate.png){:class="img-responsive"}

* You can still change it to your custom name even when you're done creating it but Yes you need to be consistent when going through this process, as you might be able to change other team member's droplet name it is Therefore a must to be able to identify the exact droplet you created before taking any further action.

NB.`If not sure which droplet do you own from the default digital Ocean droplet name, do ask any of codeX Mentors or Check your digital Ocean recent emails you received on your mailbox which is the email that you used to sign in on Digital Ocean.`

<br />
<h3>Step Eight — Create Your Droplet</h3>
![image-title-here](/img/posts_Schematics/createdropletbutton.png){:class="img-responsive"}

<p>Once you have selected all of your preferred options,<code>08</code>. click on "Create".
After your Droplet is created, its root password will arrive in your email inbox and the Droplet will be set up. If you included an SSH key in the previous steps, you will not be emailed a root password — use your SSH private key to authenticate as the root user instead.</p>

:smiley: With that, your server is ready !
