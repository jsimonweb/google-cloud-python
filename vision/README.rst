Python Client for Google Cloud Vision
=====================================

|beta| |pypi| |versions| |compat_check_pypi| |compat_check_github|

The `Google Cloud Vision`_  API enables developers to
understand the content of an image by encapsulating powerful machine
learning models in an easy to use REST API. It quickly classifies images
into thousands of categories (e.g., "sailboat", "lion", "Eiffel Tower"),
detects individual objects and faces within images, and finds and reads
printed words contained within images. You can build metadata on your
image catalog, moderate offensive content, or enable new marketing
scenarios through image sentiment analysis. Analyze images uploaded
in the request or integrate with your image storage on Google Cloud
Storage.

- `Client Library Documentation`_
- `Product Documentation`_

.. |beta| image:: https://img.shields.io/badge/support-beta-silver.svg
   :target: https://github.com/googleapis/google-cloud-python/blob/master/README.rst#beta-support
.. |pypi| image:: https://img.shields.io/pypi/v/google-cloud-vision.svg
   :target: https://pypi.org/project/google-cloud-vision/
.. |versions| image:: https://img.shields.io/pypi/pyversions/google-cloud-vision.svg
   :target: https://pypi.org/project/google-cloud-vision/
.. |compat_check_pypi| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=google-cloud-vision
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=google-cloud-vision
.. |compat_check_github| image:: https://python-compatibility-tools.appspot.com/one_badge_image?package=git%2Bgit%3A//github.com/googleapis/google-cloud-python.git%23subdirectory%3Dvision
   :target: https://python-compatibility-tools.appspot.com/one_badge_target?package=git%2Bgit%3A//github.com/googleapis/google-cloud-python.git%23subdirectory%3Dvision
.. _Vision: https://cloud.google.com/vision/

.. _Google Cloud Vision: https://cloud.google.com/vision/
.. _Client Library Documentation: https://googleapis.github.io/google-cloud-python/latest/vision/
.. _Product Documentation: https://cloud.google.com/vision/reference/rest/


Quick Start
-----------

In order to use this library, you first need to go through the following steps:

1. `Select or create a Cloud Platform project.`_
2. `Enable billing for your project.`_
3. `Enable the Google Cloud Vision API.`_
4. `Setup Authentication.`_

.. _Select or create a Cloud Platform project.: https://console.cloud.google.com/project
.. _Enable billing for your project.: https://cloud.google.com/billing/docs/how-to/modify-project#enable_billing_for_a_project
.. _Enable the Google Cloud Vision API.:  https://cloud.google.com/vision
.. _Setup Authentication.: https://googleapis.github.io/google-cloud-python/latest/core/auth.html

Installation
~~~~~~~~~~~~

Install this library in a `virtualenv`_ using pip. `virtualenv`_ is a tool to
create isolated Python environments. The basic problem it addresses is one of
dependencies and versions, and indirectly permissions.

With `virtualenv`_, it's possible to install this library without needing system
install permissions, and without clashing with the installed system
dependencies.

.. _`virtualenv`: https://virtualenv.pypa.io/en/latest/


Supported Python Versions
^^^^^^^^^^^^^^^^^^^^^^^^^
Python >= 3.5

Deprecated Python Versions
^^^^^^^^^^^^^^^^^^^^^^^^^^
Python == 2.7. Python 2.7 support will be removed on January 1, 2020.


Mac/Linux
^^^^^^^^^

.. code-block:: console

    pip install virtualenv
    virtualenv <your-env>
    source <your-env>/bin/activate
    <your-env>/bin/pip install google-cloud-vision


Windows
^^^^^^^

.. code-block:: console

    pip install virtualenv
    virtualenv <your-env>
    <your-env>\Scripts\activate
    <your-env>\Scripts\pip.exe install google-cloud-vision


Example Usage
~~~~~~~~~~~~~

.. code-block:: python

   from google.cloud import vision

   client = vision.ImageAnnotatorClient()
   response = client.annotate_image({
     'image': {'source': {'image_uri': 'gs://my-test-bucket/image.jpg'}},
     'features': [{'type': vision.enums.Feature.Type.FACE_DETECTION}],
   })

Next Steps
~~~~~~~~~~

-  Read the `Client Library Documentation`_ for Google Cloud Vision API
   API to see other available methods on the client.
-  Read the `Product documentation`_ to learn
   more about the product and see How-to Guides.
