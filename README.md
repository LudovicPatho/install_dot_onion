# install_dot_onion

1.   **Install Tor:**
      - Install the Tor Browser on your system. You can download it from the official Tor Project website.

3.   **Configure the Web Server:**  
      - Set up a web server on your machine. Apache is a common choice, but you can use other web servers based on your preferences.

4.   **Create the HTML Page:**
      - Create a simple HTML page that you want to host. Save it in the directory of your web server.

5.   **Configure the Web Server for Tor:**
      - Modify the configuration of your web server to listen on port 80 and possibly port 443 (for HTTPS traffic).
      - Ensure that your server is configured to accept connections from localhost.

5.   **Configure the Tor Hidden Service File:**
      - Create a configuration file for your .onion service. You can do this by adding the following lines in the torrc file (the Tor configuration file):
                 
        ```
        HiddenServiceDir /path/to/hidden_service_directory 
        HiddenServicePort 80 127.0.0.1:80
        ```
      - Make sure to replace "/path/to/hidden\_service\_directory" with the actual path to your Hidden Service directory.
        
6.   **Restart Tor:**
      - Restart the Tor service to apply the configuration changes.

7.   **Access Your .onion Site:**
      - Once Tor is restarted, you will find a private key in the Hidden Service directory. Use this private key to access your .onion site via the Tor Browser.
