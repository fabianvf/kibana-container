# Role Name

[![Build Status](https://travis-ci.org/chouseknecht/kibana-container.svg?branch=master)](https://travis-ci.org/chouseknecht/kibana-container)

Adds a kibana service to your [Ansible Container](https://github.com/ansible/ansible-container) project. Run the following commands
to install the service:

```
# Set the working directory to your Ansible Container project root
$ cd myproject

# Install the service
$ ansible-container install <USERNAME.ROLE_NAME>
```

## Requirements

- [Ansible Container](https://github.com/ansible/ansible-container)
- An existing Ansible Container project. To create a project, simply run the following:
    ```
    # Create an empty project directory
    $ mkdir myproject

    # Set the working directory to the new directory
    $ cd myproject

    # Initialize the project
    $ ansible-contiainer init
    ```

## Role Variables

kibana_host: 0.0.0.0
> IP address or host name to bind the Kibana server to.  

kibana_port: 5601
> The port the Kibana server listens on.

kibana_elasticsearch_url: http://elasticsearch:9200
> The URL of your Elasticsearch server.

kibana_index: .kibana
> Kibana uses an index in Elasticsearch to store saved searches, visualizations and dashboards. It will create a new index if it doesn't already exist.

kibana_log_dest: stdout
> By default logging is sent to *stdout*. If prefered, logging can be sent to a file path such as */var/log/kibanan/kibana.log*.  

kibana_logging_silent: false
> Suppress all logging output.

kibana_logging_quiet: false
> Suppress all logging output except errors.

kibana_logging_verbose: true
> Log all events, including system usage information and all requests.

## License

Apache v2

## Author Information

[@chouseknecht](https://github.com/chouseknecht)

