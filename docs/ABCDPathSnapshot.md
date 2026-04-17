# ABCDPathSnapshot

Snapshot of a single ABCD path reference at trigger time.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**path_part_id** | **UUID** |  | 
**materialized_path** | **str** |  | 
**part_type** | [**PartType**](PartType.md) |  | 

## Example

```python
from ksapi.models.abcd_path_snapshot import ABCDPathSnapshot

# TODO update the JSON string below
json = "{}"
# create an instance of ABCDPathSnapshot from a JSON string
abcd_path_snapshot_instance = ABCDPathSnapshot.from_json(json)
# print the JSON string representation of the object
print(ABCDPathSnapshot.to_json())

# convert the object into a dict
abcd_path_snapshot_dict = abcd_path_snapshot_instance.to_dict()
# create an instance of ABCDPathSnapshot from a dict
abcd_path_snapshot_from_dict = ABCDPathSnapshot.from_dict(abcd_path_snapshot_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


