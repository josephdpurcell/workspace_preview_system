## Developer Install

### Build the codebase

    composer install

This will create a docroot folder that contains drupal and the WPS profile

### Install WPS

    phing install

`phing install` assumes:

DB username: `root`  
DB pass: `<none>`  
DB host: `localhost`  
DB Name: `workspace_preview_system`

You can override the presets with `-Ddb.<option>=<value>`. For example, to
change the DB name:

    -Ddb.name=my_db_name

### Pull changes

If you make changes to the profile within the docroot directory and you want to
pull them back into the top-level directory so they can be committed to VCS, use
the `phing pull` command:

    phing pull

## Push changes

Alternately, you can push changes in the top-level down into the docroot with
`phing push`

    phing push

