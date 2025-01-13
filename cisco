provider "ciscoasa" {
  # Replace with your Cisco ASA connection details
  hostname = "<ASA_HOSTNAME_OR_IP>"
  username = "<USERNAME>"
  password = "<PASSWORD>"
  insecure = true # Set to true if using self-signed certificates
}

resource "ciscoasa_access_rule" "example_rule" {
  name = "Allow_Traffic"

  # Define the ACL name (e.g., interface name or global ACL)
  acl = "outside_access_in"

  # Source configuration
  source_networks = ["192.168.1.0/24"]

  # Destination configuration
  destination_networks = ["10.0.0.0/24"]

  # Protocol and port (set protocol to "any" to allow all protocols)
  protocol = "tcp"
  destination_ports = ["80", "443"]

  # Action: permit or deny
  action = "permit"

  # Specify rule priority/order
  position = 100
}
