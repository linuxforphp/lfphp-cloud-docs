.. _GettingStartedAnchor:

Getting started
===============

.. index:: Getting started

The LfPHP Cloud offers a simple way to get you online, as quickly and as easily as possible: one-click application publishing.

.. index:: Dashboard

Dashboard
---------

The LfPHP Cloud Services' **Dashboard** offers convenient one-click options to set up many kinds of website,
spin up many types of service, add domains and secure them using SSL, and much more!

.. figure:: /images/Dashboard.png
   :alt: The Dashboard

   The Dashboard

The main options offered on the Dashboard are:

- :ref:`status`
- :ref:`server_configuration`
- :ref:`domains`
- :ref:`security`
- :ref:`access_tokens`
- :ref:`one-click_apps`
- :ref:`lambda_cloud`
- :ref:`backups`
- :ref:`logs`
- :ref:`statistics`
- :ref:`file_browser`

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
:ref:`file_browser` of your hosting server and your MariaDB (MySQL) databases through the
`phpMyAdmin <https://www.phpmyadmin.net/>`_ Web interface. Moreover, you'll have the ability to reset
the hosting access password (not your main account password) by clicking on the
``Reset Access Password`` button.

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

.. note:: Once the domain resolves itself to your hosting server, the domain name will automatically be secured with a **Let's Encrypt** certificate (see :ref:`security`).

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
**Linux for Composer** (`<https://linuxforphp.com/files/guides/file.pdf>`_).

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

   Installation confirmation

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

.. _backups:

Backups
-------

.. index:: Backups

The **Backups** section makes it possible to generate and download a ZIP file containing all of
the files of the :ref:`one-click_apps`.

.. figure:: /images/Backup_Success.png
   :alt: A backup was successfully generated

   A backup was successfully generated

.. note:: Backups or your databases must be done through the phpMyAdmin interface. The databases are NOT included in these backups!

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

.. _file_browser:

File Browser
------------

.. index:: File browser

If you have installed one of the :ref:`one-click_apps`, you will be able to access the file system of
your app in the **File browser** that can be found in the :ref:`status` section. Using this utility,
you can move, copy, edit, delete, upload, or zip archive specific files or folders. You can also restore
backups of your files using the LfPHP file browser.

.. figure:: /images/File_Browser.png
   :alt: The File browser

   The File browser

.. index:: Crons

If you access the **File browser**, you will notice that you can access the **Cron** files from the
root folder. You can therefore edit the cron files if you need to run certain tasks at certain intervals
of time on your hosting account.

.. figure:: /images/Crons.png
   :alt: The Cron files

   The Cron files

Here is an example on how to execute a cURL request to run the cron job of a **Drupal** installation:

.. code-block:: bash

    curl http://myaccount.linuxforphp.com/cron/qH9iYDiCQPcouUbws1iasCMVhOERUq99bIFOLlUe4KAMfs9eSH1yvmSgCvLA9g

.. note:: All cron jobs are run as the user 'root' on the hosting server.