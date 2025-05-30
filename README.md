## iPXE based deployment server
This role installs and configures all required components to deploy OS images to systems that support iPXE.

This role will configure:

  * DHCP for network addressing and configuration
  * TFTP to deploy the iPXE bootloader
  * HTTP to serve iPXE menus and OS images that are to be deployed
    * By default the server will not use SSL, this can be enabled

The following tools are also automatically provided for system diagnosis/decommissioning:

  * Memtest86+ 7.00 memory diagnostics
  * ShredOS disk sanitizer

For the src_url rsync functionality to work, you need to configure a SSH key that can access the desired remote server in order to sync images to the deployment server.

The iPXE menus also contain a help page that can be configured to show the email/phone details for a helpdesk to guide endusers when necessary.

This server is mainly aimed for deploying Device Edge images built on a remote OSbuild-composer Image Builder, and might not (yet?) be suitable for deploying other OS images.
