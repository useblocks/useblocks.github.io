Install
-------
::

    gem install bundler jekyll webrick

    export PATH=$PATH:/home/daniel/.gem/ruby/3.0.0/bin
    # or
    export PATH=$PATH:/home/daniel/.local/share/gem/ruby/3.0.0/bin

    bundle update

Run
---
::

    bundle exec jekyll serve

Jobs
----

Jobs can be found under ``_jobs``.

Do not use ``_data``, this approach is not followed anymore.

To deactivate a job, add ``_`` as prefix to the file name.


Team members
------------
Team members can be added under ``_team``.

HTML changes need to be done in `_layouts/team_members` for the member page

Member image is set via css currently.
In `useblocks.css` there must be an entry for the `first_name` attribute:

::
  
  #daniel {
    background: url(/assets/img/daniel_kreis_transparent.png) no-repeat center;
    border: 5px solid #333333;
  }

.. note::
  
   So the `image` option has no effect, yet. But this will be changed in future
