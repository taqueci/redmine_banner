# Redmine Banner Plugin 

Plugin to show site-wide message from site administrator, such as maintenance
information or notifications.

Build Status: [![wercker status](https://app.wercker.com/status/d9d99ba1334f550bd82fd6ae5218523f/s/master "wercker status")](https://app.wercker.com/project/byKey/d9d99ba1334f550bd82fd6ae5218523f)

### Plugin installation

#### For Redmine 2.x:

For Redmine 2.1 or later, please use Version 0.0.8 or later. For Redmine 2.0,
please use Version 0.0.7.

1.  Copy the plugin directory into the plugins directory.
2.  Run the migration task.  e.g. rake redmine:plugins:migrate
    RAILS_ENV=production  (For Redmine 2.x)
3.  (Re)start Redmine.


Version 0.0.5 later, migration is required.

#### For Redmine 1.x:

For Redmine 1.x, please use version 0.0.6.

1.  Copy the plugin directory into the vendor/plugins directory.
2.  Run the migration task. e.g. rake db:migrate_plugins RAILS_ENV=production
    (For Redmine 1.x)
3.  (Re)start Redmine.


### Uninstall

For Redmine 2.x, use the following command:

*   rake redmine:plugins:migrate NAME=redmine_banner VERSION=0
    RAILS_ENV=production


For Redmine 1.x, use the following command:

*   rake db:migrate_plugins NAME=redmine_banner VERSION=0 RAILS_ENV=production


### Usage for site wide banner

1.  Go to plugin's page and click "Settings" link of Redmine Banner Plugin.
    You can edit banner message and select style for message. Also you can
    access setting page from administration menu, click "banner" icon. 


### Usage for project scope banner

1.  Banner can be used as project module. If you want to manage the banner for
    your project, "Manage Banner" permission is required to your role.

2.  Go to project settings tab and check "Banner" as project module.
3.  Then you can see "Banner" tab on project settings page.


### Current limitations

1.  Banner for each project does not support timer.
2.  Banner for each project is located at the top of the project only. (Not
    support footer)
3.  To render banner, javascript (prototype.js) is required and banner will
    not be shown correctly if you does not use modern browser.



### Note

    To use this plugin with older Redmine versions (1.xx, 1.0.x...), please see this instruction.
    https://github.com/akiko-pusu/redmine_banner/wiki/How-to-use-this-plugin-previous-version-(1.xx,-1.0.x...)

## Changelog

### 0.1.2

*   Fix style and css selector. (Github: #45)
*   Change global banner style for responsive mode. (Github: #68)
*   Code refactoring.
*   Fix: Prevent deprecation warning. (Github PR: #60) Thanks, Wojciech.
*   Refactor: Rename file to prevent conflict (Github #63 / r-labs: 54).
*   i18n: Update Italian translation file. (Github: #61 / r-labs: 57) Thanks,
    R-i-c-k-y.
*   i18n: Add Spanish translation file. (Github: #61 / r-labs: 52) Thanks
    Picazamora!
*   i18n: Update Turkish translation file. (Github: #64) Thank you so much,
    Adnan.
*   i18n: Update Portuguese translation file. (Github: #50) Thanks, Guilherme.


### 0.1.1

*   Support Redmine 3.x.
*   Update some translation files. Bulgarian, German. Thank you so much, Ivan
    Cenov, Daniel Felix.
*   Change column type of banner_description from string to text.Thank you so
    much Namezero. (#44)


### 0.1.0

*   Fixed bug: Global banner timer does not work. (r-labs: #1337)
*   Feature: Add related link field for more information to Global Banner.
    (r-labs: #1339)
*   i18n: Update Korean translation file. (r-labs: #1329) Thank you so much,
    Ki Won Kim.


### 0.0.9

*   Authenticated users can turn off global banner in their session.
*   Add option to show global banner only for authenticated users.
*   Add option to show only at the login page.
*   Code refactoring.
*   Italian translation was contributed by @R-i-c-k-y.
*   French translation was contributed by Laurent HADJADJ.


### 0.0.8

*   Support Redmine 2.1. (Redmine 2.0.x is no longer supported. Please use
    version 0.0.7 for Redmine 2.0.x) 


### 0.0.7

*   Compatible with Redmine 2.0.0


### 0.0.6

*   Fixed bug: Project banner should be off when module turned disabled.
*   Fixed bug: In some situation, "ActionView::TemplateError undefined method
    is_action_to_display" is happened.
*   Update Russian Translation. Thank you so much, Александр Ананьев.


### 0.0.5

*   Support banner for each project. Thank you so much, Denny Schäfer, Haru
    Iida.


### 0.0.4

*   Support timer function.
*   Add links to turn off or modify banner message quickly. (Links are shown
    to Administrator only) 


### 0.0.3

*   Code refactoring. Stop to override base.rhtml and use javascript. Great
    thanks, Haru Iida-san. Also, remove some "To-Do" section of README.

*   Add translations. Russian, German, Brazilian Portugues. Thank you so much,
    Александр Ананьев, Denny Schäfer, Maiko de Andrade!


### 0.0.2

*   Support i18n.


### 0.0.1

*   First release


### Repository

*   https://github.com/akiko-pusu/redmine_banner


### WebPage

*   http://www.r-labs.org/projects/banner (Project Page)


### License

This software is licensed under the GNU GPL v2. See COPYRIGHT and COPYING for
details. 
