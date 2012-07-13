## Description

This class can be used to help quickly register new Custom Post Types, Taxonomies and Meta Boxes. Based off of tutorials from Tuts+ Premium and WPtuts+ (Links listed below).

*Requires* PHP 5.3 or greater.

### Usage

Download the class, and drag it into your theme directory. 

Next, within `functions.php`, require the class:

    require 'custom-post-helper.php';

#### Create Custom Post Type

Instantiate the Custom_Post_Type helper class. For example, if you want a Project post type, you would type:

    $project = new Custom_Post_Type('Project');

#### Create Custom Taxonomies

Adding a taxonomy to allow filtering capabilities within your custom post type is as easy as entering the folloring line:

    $project->add_taxonomy('freelance');

#### Create Meta Boxes

Lastly, you will likely want the ability to input additional info about your different posts within the new custom type. This is where the custom meta box comes in to play:

    $project->add_meta_box(
      'Client Info',
      array(
        'Client Name' => 'text',
        'Description' => 'textarea',
        'New Client' => 'checkbox',
        'Client Logo' => 'file',
        'Client Industry' => array('select', array('entertainment', 'government', 'education') )
      )
    );

### References

WPtuts+ "Custom Post Type Helper Class" - http://bit.ly/MoFIJa

Tuts+ Premium "The Magic of WordPress Custom Post Types" - http://bit.ly/MouDpJ
