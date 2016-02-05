Simple blogging application based on the following tutorial.

https://www.youtube.com/watch?v=BI_VnnOLSKY

Rails 4.0.4 with Ruby 1.9.3.

Install and Run
---------------

- Git clone into directory of choice
- CD into the root directory
- Run bundle install
- Run rake db:migrate
- To launch type rails server / rails s 


Troubelshooting
---------------

If receiving the following error when tryin to run:

ExecJS::ProgramError

try changing line in app/views/layouts/application.html.erb

<%= javascript_include_tag "applicaiton", "data-turbolinks-track" => true %>

to

<%= javascript_include_tag "default", "data-turbolinks-track" => true %>

See this Stack Overflow question for more info:

http://stackoverflow.com/questions/30116966/execjsprogramerror-in-welcomeindex-typeerror-object-doesnt-support-this-pro

If getting an ExecJS::RuntimeError make sure you have a Javascript Runtime installed on your system. Installing Node js is one way to do this.

ExecJS also supports these runtimes:

therubyracer - Google V8 embedded within Ruby

therubyrhino - Mozilla Rhino embedded within JRuby

Apple JavaScriptCore - Included with Mac OS X

Microsoft Windows Script Host (JScript)

