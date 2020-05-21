# Vulkan’s Extension Mechanism
One thing Khronos APIs are brilliant at doing is allowing Vulkan implementations to extend the normal functionality of Vulkan and add new techniques & features to the Vulkan API independently of the rest of the API and other implementations. For example, when NVIDIA’s RTX platform launched it was the first platform to feature real-time raytracing en masse alongside typical graphics workloads like Vulkan. Because NVIDIA was the first to allow raytracing with Vulkan, they had to create a specially made extension called VK_NV_ray_tracing to add this missing functionality.

If lots of Vulkan drivers support an extension (as anyone can implement any Vulkan extension provided it conforms with the original author’s intentions), the vendors involved will often work together to make a multi-vendor extension, which are prefixed with EXT (for generic multi-vendor) or KHR (for extensions by the Khronos Group). If a KHR extension sees widespread adoption, Khronos will often promote an extension into the core specification as part of a new Vulkan version, allowing it to be used anywhere where that specific version of Vulkan is supported. An example of this would be VK_KHR_get_physical_device_properties2 being promoted and included as part of Vulkan 1.1.

If the hardware and graphics driver supports the extra features defined in extensions, then the developers can query and use those extensions for their projects. All graphics card only supports a specific set of extensions, and they must be queried and enabled explicitly before accessing them. You can write it this way as an example:

```
if (VK_KHR_extension_name)
{
    // use the new cool features!
}
else
{
    // do things the old way...
}
```

Obviously it’s not that simple to check if it supports an extension, but keep that example in mind. We will discuss further approach and practices that you can use to query and enable various features that your graphic card driver may provide. Vulkan Standard is flexible in a way that drivers can extend Vulkan with custom functionality through “extensions”, which you can then query and enable to use that functionality.
