provider "google" {
  project     = "advance-river-430310-p9"
  region      = "europe-wes"
  zone        = "europe-west1-c"
}
resource "google_compute_instance" "default" {
  provider = google
  name = "default"
  machine_type = "e2-micro"
  network_interface {
    network = "default"
  }

  boot_disk {
    initialize_params {
      image = "ubuntu-os-cloud/ubuntu-2004-focal-v20220712"
    }
  }
  # Some changes require full VM restarts
  # consider disabling this flag in production
  #   depending on your needs
  allow_stopping_for_update = true
}
