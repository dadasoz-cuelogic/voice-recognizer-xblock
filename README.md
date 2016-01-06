# Voice Recognizer XBlock #
This XBlock allows students to recognize their voice and can see the what they spoke.

It supports multiple languages. This version works only on Google Chrome.

## Supported languages ##
    Afrikaans
    Bahasa Indonesia
    Bahasa Melayu
    Català
    Čeština
    Dansk
    Deutsch
    Australia
    Canada
    English - India
    English - New Zealand
    English - South Africa
    English - United Kingdom
    English - United States
    Bolivia
    Argentina
    Chile
    Colombia
    Costa
    Ecuador
    España
    Estados
    Guatemala
    Honduras
    México
    Nicaragua
    Panamá
    Paraguay
    Perú
    Puerto
    República
    Uruguay
    Venezuela
    Euskara
    Filipino
    Français
    Galego
    हिन्दी
    Hrvatski
    IsiZulu
    Íslenska
    Italiano
    Italia
    Svizzera
    Lietuvių
    Magyar
    Nederlands
    Norsk
    Polski
    Português
    Brasil
    Portugal
    Română
    Slovenščina
    Slovenčina
    Suomi
    Svenska
    Tiếng
    ภาษาไทย
    Türkçe
    Ελληνικά
    български
    Pусский
    Српски
    Українська
    한국어
    普通话 
    普通话 
    中文 
    粵語 

## Features ##
  1. Supports Multiple Languages
  2. Assesment and grading support


## Installation instructions ##
In order to install the XBlock into your Open edX devstack Server you need to:

  1. Download the XBlock from github. Place the files inside your server.
  2. Install your block:
        You must replace `/path/to/your/block` with the path where you have downloaded the XBlock

        $ vagrant ssh
        vagrant@precise64:~$ sudo -u edxapp /edx/bin/pip.edxapp install /path/to/your/block
        
  3. Enable the block:

        #.  In ``edx-platform/lms/envs/common.py``, uncomment::

            # from xmodule.x_module import prefer_xmodules
            # XBLOCK_SELECT_FUNCTION = prefer_xmodules

        #.  In ``edx-platform/cms/envs/common.py``, uncomment::

            # from xmodule.x_module import prefer_xmodules
            # XBLOCK_SELECT_FUNCTION = prefer_xmodules

        #.  In ``edx-platform/cms/envs/common.py``, change::

            'ALLOW_ALL_ADVANCED_COMPONENTS': False,

            to::

            'ALLOW_ALL_ADVANCED_COMPONENTS': True
            
  4. Add the block to your courses' advanced settings in Studio:
  

        #. Log in to Studio, and open your course
        #. Settings -> Advanced Settings
        #. Change the value for the key ``"advanced_modules"`` to ``voicerecognizer``


