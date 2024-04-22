# CrowdStrike Host Information with Discovery Injected

This is a POC python script that is slow because it iterates one host at a time. It is a proof of concept to show how to get host information from the CrowdStrike API with the Discovery API injected.

## Usage

```bash
python3 host_report.py
```

## You need the Host ID or aid for this

pythonSDK: falcon.query_hosts
https://falconpy.io/Service-Collections/Discover.html#get_hosts

```
response = falcon.command("query_hosts", filter="aid:'a67bc33987984a48be3877a21fec2895'")
```

discover/queries/hosts/v1

aid:'c67bc33987984a48be3877a21fec2895'

https://api.us-2.crowdstrike.com/discover/queries/hosts/v1?filter=aid%3A'a67bc33987984a48be3877a21fec2895'

```json
{
  "meta": {
    "query_time": 0.015367229,
    "pagination": {
      "offset": 0,
      "limit": 100,
      "total": 1
    },
    "powered_by": "discover-api",
    "trace_id": "a64b7edf-32d1-496f-b352-fc3aa0505f5d"
  },
  "resources": [
    "a5c142b66fbf46c8a94fd7d9638a612f_ATDx4DNtZ_qPENFwrpbi-To4KLracXM3P-pl0IVdTiWChw"
  ]
}
```

## You need the Discovery API ID

pythonSDK: falcon.get_hosts
```
id_list=['a5c142b66fbf46c8a94fd7d9638a612f_ATDx4DNtZ_qPENFwrpbi-To4KLracXM3P-pl0IVdTiWChw']
response = falcon.command("get_hosts", ids=id_list)
```

https://falconpy.io/Service-Collections/Discover.html#get_hosts

/discover/entities/hosts/v1

a5c142b66fbf46c8a94fd7d9638a612f_ATDx4DNtZ_qPENFwrpbi-To4KLracXM3P-pl0IVdTiWChw

https://api.us-2.crowdstrike.com/discover/entities/hosts/v1?ids=a5c142b66fbf46c8a94fd7d9638a612f_ATDx4DNtZ_qPENFwrpbi-To4KLracXM3P-pl0IVdTiWChw

```json
{
  "meta": {
    "query_time": 0.132871648,
    "powered_by": "discover-api",
    "trace_id": "a504290d-0fbc-4914-9d38-e9e1a70a197d"
  },
  "resources": [
    {
      "id": "a5c142b66fbf46c8a94fd7d9638a612f_ATDx4DNtZ_qPENFwrpbi-To4KLracXM3P-pl0IVdTiWChw",
      "field_metadata": {
        "agent_version": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "aid": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "asset_roles": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "available_disk_space": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "available_disk_space_pct": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "average_memory_usage": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "average_memory_usage_pct": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "average_processor_usage": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "bios_manufacturer": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "bios_version": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "cid": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "city": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "computed_asset_roles": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "computed_internet_exposure": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "country": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "criticality": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "current_local_ip": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "data_providers": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "data_providers_count": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "disk_sizes": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "entity_type": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "external_ip": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "field_metadata": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "first_seen_timestamp": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "form_factor": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "groups": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "hostname": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "id": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "internet_exposure": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "kernel_version": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "last_seen_timestamp": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "local_ip_addresses": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "local_ips_count": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "logical_core_count": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "mac_addresses": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "max_memory_usage": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "max_memory_usage_pct": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "max_processor_usage": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "network_interfaces": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "number_of_disk_drives": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "os_version": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "override_asset_roles": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "override_criticality_rules": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "override_internet_exposure": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "physical_core_count": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "platform_name": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "processor_package_count": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "product_type_desc": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "reduced_functionality_mode": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "system_manufacturer": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "system_product_name": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "system_serial_number": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "tags": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "total_disk_space": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "total_memory": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "used_disk_space": {
          "providers": [
            "CrowdStrike"
          ]
        },
        "used_disk_space_pct": {
          "providers": [
            "CrowdStrike"
          ]
        }
      },
      "cid": "abcdefg66fbf46c8a94fd7d9638a612f",
      "aid": "abcdefg987984a48be3877a21fec2895",
      "entity_type": "managed",
      "first_seen_timestamp": "2024-04-18T08:44:35Z",
      "last_seen_timestamp": "2024-04-22T13:00:00Z",
      "country": "Norway",
      "city": "Oslo",
      "platform_name": "Linux",
      "os_version": "Debian GNU 11",
      "kernel_version": "5.10.0",
      "product_type_desc": "Server",
      "tags": [
        "SensorGroupingTags/BLAH"
      ],
      "groups": [
        "1eea275d44944d9bbe5262bb8336433b"
      ],
      "agent_version": "7.13.16604.0",
      "system_product_name": "VMware Virtual Platform",
      "system_manufacturer": "VMware, Inc.",
      "system_serial_number": "VMware-42 13 64 f9 8a a9 76 bd-14 fc 08 b2 6e 39 2d 01",
      "bios_manufacturer": "Phoenix Technologies LTD",
      "bios_version": "6.00",
      "external_ip": "91.206.34.200",
      "hostname": "ls-debian11",
      "local_ips_count": 1,
      "network_interfaces": [
        {
          "local_ip": "10.255.1.208",
          "mac_address": "00-50-56-93-D7-C1",
          "interface_alias": "ens192",
          "network_prefix": "10.255"
        }
      ],
      "os_security": {},
      "current_local_ip": "10.255.1.208",
      "reduced_functionality_mode": "No",
      "form_factor": "Virtual machine",
      "data_providers": [
        "CrowdStrike"
      ],
      "data_providers_count": 1,
      "mac_addresses": [
        "00-50-56-93-D7-C1"
      ],
      "local_ip_addresses": [
        "10.255.1.208"
      ],
      "mount_storage_info": [
        {
          "mount_path": "/",
          "used_space": 6,
          "available_space": 12
        }
      ],
      "disk_sizes": [
        {
          "disk_name": "sda",
          "disk_space": 20
        }
      ],
      "number_of_disk_drives": 1,
      "cpu_processor_name": "Intel(R) Xeon(R) Platinum 8268 CPU @ 2.90GHz",
      "processor_package_count": 2,
      "physical_core_count": 2,
      "logical_core_count": 2,
      "total_memory": 3919,
      "total_disk_space": 20,
      "average_processor_usage": 1,
      "max_processor_usage": 2,
      "average_memory_usage": 1816,
      "average_memory_usage_pct": 46,
      "max_memory_usage": 1817,
      "max_memory_usage_pct": 46,
      "used_disk_space": 6,
      "used_disk_space_pct": 30,
      "available_disk_space": 12,
      "available_disk_space_pct": 60,
      "criticality": "Unassigned",
      "asset_roles": [
        "FTP server",
        "SSH server",
        "Highly connected"
      ],
      "computed_asset_roles": [
        "FTP server",
        "SSH server",
        "Highly connected"
      ],
      "override_criticality_rules": false,
      "override_asset_roles": false,
      "internet_exposure": "Pending",
      "computed_internet_exposure": "Pending",
      "override_internet_exposure": false,
      "discovering_by": [
        "Passive"
      ],
      "active_discovery": {
        "networks": [
          {
            "id": "abc25783cf3c5d26b1d7ab71bd2859c3"
          }
        ]
      }
    }
  ]
}
```