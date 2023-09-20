+++
title = 'prep'
layout = 'prep'
emoji= '📝'
menu_level = ['week']
weight = 1
coursework= 'Module-cloud'
coursework_filter= 'Week 4'
+++

## Setup Terraform on Mac and Linux

### Mac Installation Steps

1. **Download the Terraform Binary**: Go to the [Terraform Downloads Page](https://developer.hashicorp.com/terraform/downloads) and download the package suitable for your macOS system.

2. **Unzip the Package**: Open your terminal and run:

```bash
unzip ~/Downloads/terraform_*_darwin_amd64.zip
```

Replace `*` with the downloaded version.

3. **Move to /usr/local/bin**: This allows any user to run the Terraform command.

```bash
mv terraform /usr/local/bin/
```

4. **Check the Installation**: Confirm Terraform is installed correctly.

```bash
terraform --version
```

### Linux Installation Steps

1. **Download the Terraform Binary**: Go to the [Terraform Downloads Page](https://developer.hashicorp.com/terraform/downloads) and download the package suitable for your Linux system.

2. **Unzip the Package**: Open your terminal and run:

```bash
unzip ~/Downloads/terraform_*_linux_amd64.zip
```

Replace `*` with the downloaded version.

3. **Move to /usr/local/bin**: This makes the `terraform` command globally accessible.

```bash
sudo mv terraform /usr/local/bin/
```

4. **Check the Installation**: Confirm Terraform is installed correctly.

```bash
terraform --version
```

For more detailed instructions, you can refer to the [Terraform Installation Documentation](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli).
