# addnagios
add host CLient01 Server to Server Nagios

# Ubuntu Host configuration file1

define host {
        use                          linux-server
        host_name                    client01
        alias                        Ubuntu Host
        address                      ip-private-Client01
        register                     1
}

define service {
      host_name                       client01
      service_description             PING
      check_command                   check_nrpe!check_ping
      max_check_attempts              2
      check_interval                  2
      retry_interval                  2
      check_period                    24x7
      check_freshness                 1
      contact_groups                  admins
      notification_interval           2
      notification_period             24x7
      notifications_enabled           1
      register                        1
}

define service {
      host_name                       client01
      service_description             Check Users
      check_command                   check_nrpe!check_users
      max_check_attempts              2
      check_interval                  2
      retry_interval                  2
      check_period                    24x7
      check_freshness                 1
      contact_groups                  admins
      notification_interval           2
      notification_period             24x7
      notifications_enabled           1
      register                        1
}

define service {
      host_name                       client01
      service_description             Check SSH
      check_command                   check_nrpe!check_ssh
      max_check_attempts              2
      check_interval                  2
      retry_interval                  2
      check_period                    24x7
      check_freshness                 1
      contact_groups                  admins
      notification_interval           2
      notification_period             24x7
      notifications_enabled           1
      register                        1
}

define service {
      host_name                       client01
      service_description             Check Root / Disk
      check_command                   check_nrpe!check_root
      max_check_attempts              2
      check_interval                  2
      retry_interval                  2
      check_period                    24x7
      check_freshness                 1
      contact_groups                  admins
      notification_interval           2
      notification_period             24x7
      notifications_enabled           1
      register                        1
}

define service {
      host_name                       client01
      service_description             Check APT Update
      check_command                   check_nrpe!check_apt
      max_check_attempts              2
      check_interval                  2
      retry_interval                  2
      check_period                    24x7
      check_freshness                 1
      contact_groups                  admins
      notification_interval           2
      notification_period             24x7
      notifications_enabled           1
      register                        1
}

define service {
      host_name                       client01
      service_description             Check HTTP
      check_command                   check_nrpe!check_http
      max_check_attempts              2
      check_interval                  2
      retry_interval                  2
      check_period                    24x7
      check_freshness                 1
      contact_groups                  admins
      notification_interval           2
      notification_period             24x7
      notifications_enabled           1
      register                        1
}
