# Installation of local development environment for Wordpress

1. Download bitnami wordpress stack

    http://bitnami.org/stack/wordpress

2. Install the bitnami package. Keep all the defaults. Choose launching the wordpress stack at the end. You should have an instance of wordpress running at:

    http://172.16.50.1:8080/wordpress/

    The administration panel is at:

    http://172.16.50.1:8080/wordpress/wp-admin
    
     (you should use the login/password set in the installation process):
    
    
3. Clone the git repository in the directory you want to work. Assuming your working directory is `~/work`
        
        cd ~/work                                                      
        git clone git@github.com:jorgemanrubia/zendone-blog.git

    This will create a directory `zendone-blog` in your working directory.
    
    You can create a textmate project by dragging the created `zendone-blog` folder to the Textmate icon. Then choose `File->Save Project As` in order to save the project file.
    
4. Go to the directory where you installed wordpress locally (note that the version can change). Then, Link your working directory into this directory:

        cd /Applications/wordpress-3.1.3-0/apps/wordpress/htdocs/wp-content/themes
        ln -s ~/work/zendone-blog/zendone-theme/ zendone-theme

    This will allow you to select the theme in the wordpress admin panel. When you edit the theme in '~/work/zendone-blog' changes will be reflected in the browser.