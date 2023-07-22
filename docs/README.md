
The OpenStack Packer plugin provides a builder that is able to create new images
for use with OpenStack. The builder takes a source image, runs any provisioning
necessary on the image after launching it, then creates a new reusable image.
This reusable image can then be used as the foundation of new servers that are
launched within OpenStack. The builder will create temporary keypairs that
provide temporary access to the server while the image is being created. This
simplifies configuration quite a bit.

## Installation

Packer v1.7.0 and later

```hcl
packer {
  required_plugins {
    openstack = {
      version = "~> 1"
      source  = "github.com/hashicorp/openstack"
    }
  }
}
```

### Components

#### Builder

- [builder](packer/integrations/BrandonRomano/openstack/latest/components/builder/openstack) - The OpenStack Packer builder is able to create new images for use with OpenStack.
