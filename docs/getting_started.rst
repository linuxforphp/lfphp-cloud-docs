.. _GettingStartedAnchor:

Getting started
===============

.. index:: Getting started

The LfPHP Cloud offers a simple way to get you online, as quickly and as easily as possible, with one-click application publishing.

.. index:: Dashboard

Dashboard
---------

The LfPHP Cloud Services' **Dashboard** offers convenient one-click options to set up many kinds of websites,
to spin up many types of service and secure them using SSL, to add domains, email accounts, and much more!

.. figure:: /images/Dashboard.png
   :alt: The Dashboard

   The Dashboard

The main options offered on the Dashboard are:

- :ref:`status`
- :ref:`filebrowser`
- :ref:`server_configuration`
- :ref:`one-click_apps`
- :ref:`lambda_cloud`
- :ref:`domains`
- :ref:`security`
- :ref:`email`
- :ref:`access_tokens`
- :ref:`backups`
- :ref:`logs`
- :ref:`statistics`
- :ref:`ssh_access`

.. _status:

Status
------

.. index:: Status

The **Status** section allows you to see the current status of your hosting server. It also makes it possible
to view your website, get information on the physical location of the hosting server, renew your account
for an **additional** year, clear the storage area of your hosting account, and restart the server
if need be.

.. figure:: /images/Status.png
   :alt: The Status section

   Status of the hosting server

If you've deployed your website using one of our one-click apps, you will also be able to access the
:ref:`filebrowser` of your hosting server and your MariaDB (MySQL) databases through the
`phpMyAdmin <https://www.phpmyadmin.net/>`_ Web interface. Moreover, you'll have the ability to reset
the hosting access password (not your main account password) by clicking on the
``Reset Access Password`` button.

.. _filebrowser:

FileBrowser
-----------

.. index:: File browser

If you have installed one of the :ref:`one-click_apps`, or you are using a **Linux for PHP** Docker image with
the ``lfphp`` startup command, you will be able to access the file system of your hosting account in the **FileBrowser**
that can be found in the :ref:`status` section. Using this utility, you will be able to move, copy, edit, delete, upload,
zip, or unzip specific files or folders. The **LfPHP FileBrowser** also makes it very easy for you to restore archived backups.

.. figure:: /images/File_Browser.png
   :alt: The FileBrowser

   The FileBrowser Application

.. _crons:

.. index:: Crons

If you access the **FileBrowser**, you will notice that you can access the **crons** folder from the
root folder. You can therefore edit the cron files if you need to run certain tasks at certain intervals
of time on your hosting account.

.. figure:: /images/Crons.png
   :alt: The Cron files

   The Cron files

Here is an example on how to execute a cURL request to run the cron job of a **Drupal** installation:

.. code-block:: bash

    curl http://myaccount.linuxforphp.com/cron/qH9iYDiCQPcouUbws1iasCMVhOERUq99bIFOLlUe4KAMfs9eSH1yvmSgCvLA9g

.. note:: All cron jobs are run as the user 'root' on the hosting server.

.. _server_configuration:

Server Configuration
--------------------

.. index:: Server configuration

The **Server Configuration** section makes it possible to decide which version of PHP you want to
use on your hosting server, and which services, like PostgreSQL, Redis, or MongoDB, you want to make
available on your server.

.. figure:: /images/Server_Configuration.png
   :alt: Server configuration options

   Server configuration options

.. note:: The 'Default' PHP version will always correspond to the optimal version of the one-click app that you're deploying to your hosting server.

.. _one-click_apps:

One-Click Apps
--------------

.. index:: One-click apps

The **One-Click Apps** section allows you to publish your website by choosing from many kinds of websites,
depending on your set publication goal. From ecommerce websites to blogs, from wikis to traditional websites,
the LfPHP Cloud offers it all from the tip of a single mouse click!

.. figure:: /images/One-Click_Apps.png
   :alt: List of one-click apps

   List of one-click apps

Once you click on one of the ``Install`` buttons, the system will warn you that it is about to delete any
data in your hosting account before installing your new one-click app. If you need to save any data before
you continue, please ``Cancel`` the operation and save your data (see :ref:`backups`).

.. figure:: /images/One-Click_Apps_Warning.png
   :alt: Installation confirmation

   Installation confirmation

Once you confirm that you want to publish your new app, the system will start installing your application
on your hosting account.

.. figure:: /images/One-Click_Apps_Deploy_Success.png
   :alt: Deployment success message

   Deployment success message

.. note:: If you get an error message, please refresh the page and try again. If it still fails, please contact our customer support.

If you now go to the :ref:`status` section, you should see that the system is now waiting for the installation
process to finish.

.. figure:: /images/One-Click_Apps_Deploy_Status_Applying.png
   :alt: Applying changes to the hosting account

   Applying changes to the hosting account

Once your website is ready, the status will change, and you will be able to access your new website in order
to complete the final details of the installation.

.. figure:: /images/Status.png
   :alt: New app is available

   New app is available

For more information, please read our guide on how to create an instant ecommerce website using the LfPHP Cloud
(`<https://linuxforphp.com/doc/guides/how-to-create-an-instant-ecommerce-website-using-lfphp-cloud-services.pdf>`_).

.. _lambda_cloud:

PHP Lambda Cloud
----------------

.. index:: Lambda Cloud

The **PHP Lambda Cloud** section allows you to create Function-as-a-Service (FaaS) Web pages.

.. figure:: /images/Lambda.png
   :alt: PHP Lambda Cloud

   PHP Lambda Cloud

Once you click on the ``Install`` button, the system will warn you that it is about to delete any
data in your hosting account before installing your new Lambda Cloud app. If you need to save
any data before you continue, please ``Cancel`` the operation and save your data (see :ref:`backups`).
Once you confirm that you want to publish your new Lambda app, the system will start installing
your application on your hosting account.

Based on the asynchronous framework `LightMVC <https://lightmvcframework.net/>`_, and
`PSR-15 <https://www.php-fig.org/psr/psr-15/>`_ Mezzio Middleware (https://docs.mezzio.dev/),
the LfPHP Lambda Cloud empowers the PHP developer to create Web endpoints in minutes,
by simply adding, through its Web UI, the URL and the body of the Middleware function for
each created endpoint. This makes it possible to access all the facilities of a standard PHP application,
without having to set up the entire application, and all of its auxiliary services. At the click of
one single button, the developer can access SQL and NoSQL databases, a Redis cache server,
asynchronous PHP sessions, and all the other facilities one can come to expect in a standard
PHP application.

The developer can access the `PSR-7 <https://www.php-fig.org/psr/psr-7/>`_ Request and Response objects,
the entire Singleton application object, the Pimple service container, the LightMVC
`PSR-14 <https://www.php-fig.org/psr/psr-14/>`_ Event Dispatcher, which extends the
Laminas Event Manager, the Doctrine Entity Manager, the Event Sourcing and CQRS configuration settings,
and so much more!

Moreover, the developer can also return an entire HTML/CSS/JS template using his favorite
template manager. By default, LightMVC apps allow the developer to choose between three well-known
template managers: Plates, Twig, and Smarty.

.. note:: Please see the `LightMVC Framework documentation <https://lightmvc-framework.readthedocs.io/en/latest/middleware.html>`_ for more information.

Deploying new Lambda functions is as easy as clicking on the ``Add`` button, typing in the new Middleware
function and its URI/URL, and clicking on the ``Deploy`` button.

Before deplying the Middleware functions, the system will ask you to confirm that you want to overwrite
the currently deployed functions. If you need to save your previous code, click on ``Cancel``, and create
a :ref:`backups` of your code before continuing.

.. figure:: /images/Lambda_Add_Deploy_Warning.png
   :alt: Installation confirmation

   Deployment confirmation

Once you are ready to deploy, please proceed, and wait for the confirmation that your new Lambda functions
were deployed to the LfPHP Cloud.

.. figure:: /images/Lambda_Add_Deploy.png
   :alt: Lambda functions deployed

   Lambda functions deployed

Here are a few examples of Lambda functions that you can use on the LfPHP Cloud.

Firstly, let's have a look at how to access the pre-installed MariaDB (MySQL) database:

.. code-block:: php

    $queryString = $request->getServerParams()['REQUEST_URI'];

    if (preg_match('/^\/.+/', $queryString)) {
      return $handler->handle($request);
    } else {
      $app = \Ascmvc\Mvc\App::getInstance();

      $serverParams = $app->getRequest()->getServerParams();

      if (isset($serverParams['HTTP_X_REAL_IP'])) {
        $remoteAddr = $serverParams['HTTP_X_REAL_IP'];
      } else {
        $remoteAddr = $serverParams['REMOTE_ADDR'];
      }

      $response = new Laminas\Diactoros\Response();
      $response = $response->withStatus(200);
      $response->getBody()->write(
        '<p>' . strtoupper(
          'This is the NEW root lambda function!'
        ) . '<br /></p>'
      );

      $response->getBody()->write(
        '<p>You have contacted us from IP address '
        . $remoteAddr
        . '!<br /></p>'
      );

      $entityManager = $app->getServiceManager()['dem1'];

      $productsRepository = new \Application\Models\Repository\ProductsRepository(
                $entityManager,
                new \Doctrine\ORM\Mapping\ClassMetadata(
                  \Application\Models\Entity\Products::class
                )
            );

      try {
        $result = $productsRepository->find('5');

        if (!is_null($result)) {
          $results[] = $productsRepository->hydrateArray($result);
        } else {
          $results = [];
        }
      } catch (\Exception $e) {
        $results = [];
        $response->getBody()->write($e->getMessage());
      }

      $response->getBody()->write(
        '<p>' . json_encode($results[0]) . '</p>'
      );

      return $response;
    }

Secondly, here is an example of how to return a simple Response object:

.. code-block:: php

    $response = new \Laminas\Diactoros\Response();
    $response = $response->withStatus(200);
    $response->getBody()->write(phpversion());
    return $response;

Lastly, here is an example of how to access data in a MongoDB instance, and returning it
in a Response object:

.. code-block:: php

    $response = new \Laminas\Diactoros\Response();
    $response = $response->withStatus(200);

    $client = new MongoDB\Client("mongodb://localhost:27017");
    $collection = $client->demo->beers;

    //$result = $collection->insertOne(
    //  [
    //    'name' => 'Hinterland',
    //    'brewery' => 'BrewDog'
    //  ]
    //);
    //echo "Inserted with Object ID '{$result->getInsertedId()}'";

    $result = $collection->find();

    $bodyContent = '';

    foreach ($result as $entry) {
      $bodyContent .= $entry['_id'] . ': ' . $entry['name'] . '<br />' . PHP_EOL;
    }

    $response->getBody()->write($bodyContent);

    return $response;

The PHP Lambda Cloud makes it possible for the developer to build Web pages, API endpoints,
or mixed mobile application back end logic in minutes!

For more information, please read our guide on how to deploy PHP Lambda functions to the LfPHP Cloud
(`<https://linuxforphp.com/doc/guides/how-to-create-an-interactive-html-website-using-lfphp-lambda-cloud.pdf>`_).

.. _domains:

Domains
-------

.. index:: Domains

The **Domains** section gives you the option of adding domain names to your hosting account. If you do not
already own the domain name that you wish to add to your account, you can buy the domain through our own
registrar (it will require that you create an additional registrar account with us). If you do own the
domain name, you can simply modify your DNS server and have it point to the IP address that the system
will give you once you've added the name of the domain in this section.

.. figure:: /images/Domains.png
   :alt: Domain added

   Adding a domain

.. note:: Once the domain resolves itself to your hosting server, the domain name will automatically be secured with a **Let's Encrypt** certificate (see :ref:`security`). It is also possible to run your domain behind a reverse proxy service like `Cloudflare <https://www.cloudflare.com/>`_.

.. _security:

Security
--------

.. index:: Security

.. index:: SSL Certificates

The **Security** section informs you if your domain names have been secured, or not, with a
**Let's Encrypt** certificate.

.. figure:: /images/Security.png
   :alt: Security section

   Security section

If you have made sure that the domain name resolves itself correctly to your hosting server
(see :ref:`domains`), then the domain name should automatically be secured. If not,
please contact our customer service.

.. figure:: /images/Security_Success.png
   :alt: Domains were secured

   Domains were secured

.. _email:

Email Accounts
--------------

.. index:: Email Accounts

The **Email Accounts** section gives you the option of adding email accounts to your hosting account. In order
to add, delete, or modify your email accounts, you can click on the ``Email Us`` button. Once the email accounts
are added to your hosting plan, they will be displayed in this section of the page, with links to the Webmail log in
page, thus allowing you to read your email from anywhere in the World. It is also possible to set up a mail client, like
Thunderbird or your mobile phone's mail application, in order to receive your email on a specified device.

The 'General Information' sub-section gives you information on how many email accounts are still available for
your hosting plan, and offers you an easy way to modify your email accounts at any given time.

.. figure:: /images/Email.png
   :alt: Email account added

   List of email accounts associated to the current hosting account

.. note:: Once you receive an email from our customer services, you will have all of the necessary instructions to get the email accounts up and running. For example, the included instructions will tell you how to make sure that the MX record for your email domain is set to the IP of our mail servers.

.. _access_tokens:

Access Tokens
-------------

.. index:: Access Tokens

The **Access Tokens** section lets you add security tokens in order to deploy apps to your hosting server
directly from your computer's CLI, using the `Linux for Composer <https://linux-for-composer.readthedocs.io/en/latest/configuration.html#linux-for-php-cloud-mode>`_
tool. Simply add an IP address in order to deploy your application from that specific IP address.

.. figure:: /images/Access_Tokens.png
   :alt: Adding an access token

   Adding an access token

For more information, please read our guide on how to deploy Docker apps to the LfPHP Cloud using
**Linux for Composer** (`<https://linuxforphp.com/doc/guides/how-to-use-linux-for-composer-to-deploy-to-the-cloud.pdf>`_).

.. _aws_s3_bucket_sync:

AWS S3 Bucket Sync
------------------

.. index:: AWS S3 Bucket Sync

The **AWS S3 Bucket Sync** section lets you set up a folder that will sync itself with an AWS S3 bucket.

.. figure:: /images/AWS_S3_Bucket_Sync.png
   :alt: The AWS S3 Bucket Sync section

   The AWS S3 Bucket Sync section

In order to add a new synced folder to your hosting account, add the name of your S3 bucket, the Access Key ID,
the secret access key, the destination folder on your hosting account (the FileBrowser's root folder is ``/srv/tempo/``),
and check or uncheck the bidirectional feature.

.. figure:: /images/AWS_S3_Bucket_Sync_Add.png
   :alt: Adding an AWS S3 Bucket

   Adding an AWS S3 Bucket

To learn how to set up an S3 bucket, and configure the IAM access key, please see the `AWS Documentation for S3 Buckets <https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html>`_, and the `AWS Documentation for IAM <https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-quickstart.html#cli-configure-quickstart-creds>`_.

The destination folder is where you will store the synced folder. The synced folder is where you will find the files that will
be downloaded from the S3 bucket. When accessing files through the :ref:`filebrowser`, the root folder is ``/srv/tempo/``,
which is the default destination folder to store the synced folder. The destination folder can be changed according to your needs.

The bidirectional feature allows you to turn on (default) or off file mirroring. If turned on, this feature will allow you to easily
back up all of your files to your S3 bucket.

.. note:: Please note that the bidirectional feature NEVER deletes files in the S3 bucket. A manual intervention inside your S3 bucket will be necessary in order to delete unwanted files.

Once you click on the ``Add`` button, the newly added folder will appear within a few seconds.

.. figure:: /images/AWS_S3_Bucket_Sync_List.png
   :alt: The newly added AWS S3 Bucket Sync folder

   The newly added AWS S3 Bucket Sync folder

By default, the LfPHP Cloud will sync the contents of the new folder with your AWS S3 bucket every hour. The new cron
job can be found in the ``crons.hourly`` file, which is located in the ``crons`` folder. Please see the :ref:`filebrowser` section.

.. figure:: /images/Crons.png
   :alt: The Crons folder

   The Crons folder

The new cron can be modified to better suit your needs by cutting and pasting the ``/srv/awss3synccron`` command to another
cron file, thus allowing you to change how frequently the folder will be synced with your AWS S3 bucket.

.. figure:: /images/AWS_S3_Bucket_Sync_Cron.png
   :alt: The AWS S3 Bucket Sync cron job

   The AWS S3 Bucket Sync cron job

.. _continuous_delivery:

Continuous Delivery (CI/CD)
---------------------------

.. index:: Continuous Delivery

The **Continuous Delivery** section lets you add security tokens in order to deploy apps from **GitHub**,
**GitLab**, or **Bitbucket**, using webhooks and the `Linux for Composer Helper Library <https://packagist.org/packages/linuxforphp/linuxforcomposer>`_.

.. figure:: /images/Continuous_Delivery_Disabled.png
   :alt: Continuous Delivery section

   Continuous Delivery section

Simply click on the ``Enabled`` radio button for the service for which you want to set up a deployment
webhook. From there, you can create the webhook in the code repository's settings in order to start
deploying your app automatically to your hosting account.

To disable the access, click on the ``Disabled`` radio button. If you re-enable the access,
you will get a new token, and you will have to update the secret key of your repository's webhook.

.. note:: Only ``Push`` events on the ``Master`` (or ``Main``) branch will be deployed, and those requests will receive a ``201 Created`` response on successful deployment. All other events and branches will be ignored, and those requests will receive a ``204 No content`` response.

Once the webhook is set up correctly, webhook requests from the repository will be processed, and the
**LfPHP Cloud** deployment manager will look for a ``linuxforcomposer.json`` file at the root of your
repository's ``Master`` (or ``Main``) branch in order to begin deployment of your application.
To find a few ``linuxforcomposer.json`` file templates that can help you get started, please visit
our repository at `<https://github.com/linuxforphp/lfphp-cloud-templates>`_.

For more information on **Linux for Composer**, please read our guide on how to deploy Docker apps
to the LfPHP Cloud using **Linux for Composer** (`<https://linuxforphp.com/doc/guides/how-to-use-linux-for-composer-to-deploy-to-the-cloud.pdf>`_).

GitHub
^^^^^^

.. index:: GitHub Webhook

To set up a webhook for a repository hosted on **GitHub**, start by enabling the endpoint in your
**LfPHP Cloud** hosting account:

.. figure:: /images/Continuous_Delivery_Enabled_GitHub.png
   :alt: Enabling the GitHub endpoint

   Enabling the GitHub endpoint

In your **GitHub** repository's settings, add a webhook by pasting in the endpoint URL, the secret
token key, and clicking the ``Save`` button. All of the other default settings should not be modified.

.. figure:: /images/Continuous_Delivery_GitHub.png
   :alt: Adding the GitHub webhook

   Adding the GitHub webhook

GitLab
^^^^^^

.. index:: GitLab Webhook

To set up a webhook for a repository hosted on **GitLab**, start by enabling the endpoint in your
**LfPHP Cloud** hosting account:

.. figure:: /images/Continuous_Delivery_Enabled_GitLab.png
   :alt: Enabling the GitLab endpoint

   Enabling the GitLab endpoint

In your **GitLab** repository's settings, add a webhook by pasting in the endpoint URL, the secret
token key, and clicking the ``Save`` button. All of the other default settings should not be modified.

.. figure:: /images/Continuous_Delivery_GitLab.png
   :alt: Adding the GitLab webhook

   Adding the GitLab webhook

Bitbucket
^^^^^^^^^

.. index:: Bitbucket Webhook

To set up a webhook for a repository hosted on **Bitbucket**, start by enabling the endpoint in your
**LfPHP Cloud** hosting account:

.. figure:: /images/Continuous_Delivery_Enabled_Bitbucket.png
   :alt: Enabling the Bitbucket endpoint

   Enabling the Bitbucket endpoint

In your **Bitbucket** repository's settings, add a webhook by pasting in the endpoint URL, and
clicking the ``Save`` button. All of the other default settings should not be modified.

.. figure:: /images/Continuous_Delivery_Bitbucket.png
   :alt: Adding the Bitbucketwebhook

   Adding the Bitbucket webhook

.. _backups:

Backups
-------

.. index:: Backups

The **Backups** section makes it possible to generate and download a ZIP file containing all of
the files of the :ref:`one-click_apps`.

.. figure:: /images/Backup_Success.png
   :alt: A backup was successfully generated

   A backup was successfully generated

.. note:: Backups of your databases must be done through the phpMyAdmin interface. The databases are NOT included in these backups!

.. _logs:

Logs
----

.. index:: Logs

The **Logs** section gives you access to the log files of the :ref:`one-click_apps`.

.. figure:: /images/Logs.png
   :alt: Access the log files

   Access the log files

.. _statistics:

Statistics
----------

.. index:: Statistics

The **Statistics** section will allow you to access the `Webalizer <https://www.webalizer.org/>`_ records
of the :ref:`one-click_apps`.

.. figure:: /images/Statistics.png
   :alt: Access Webalizer records

   Access Webalizer records

.. _ssh_access:

SSH Access
----------

.. index:: SSH Access

The **SSH Access** section gives you the information that you need in order to access your hosting plan
from the command line. In order to gain access and obtain an SSH private key, please click on the
``Email Us`` button. Once you receive an email from our customer services, you will have all of the
necessary instructions to access your hosting plan remotely through your computer's CLI.

.. figure:: /images/SSH_Access.png
   :alt: SSH Access section

   SSH configuration details
