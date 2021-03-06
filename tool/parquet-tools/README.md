# parquet-tools
parquet-tools is a command line tool that aid in the inspection of parquet files.

## Build
cd parquet-tools && go build parquet-tools

## Example

### Output Schema

```bash
bash$ ./parquet-tools -cmd=schema -file=a.parquet
bash$
----- Go struct -----
parquet_go_root struct{
  name string
  age int32
  id int64
  weight float32
  sex bool
  day int32
}
----- Json schema -----
{
  "Tag": "name=parquet_go_root, repetitiontype=REQUIRED",
  "Fields": [
    {
      "Tag": "name=name, type=UTF8, repetitiontype=REQUIRED",
      "Fields": null
    },
    {
      "Tag": "name=age, type=INT32, repetitiontype=REQUIRED",
      "Fields": null
    },
    {
      "Tag": "name=id, type=INT64, repetitiontype=REQUIRED",
      "Fields": null
    },
    {
      "Tag": "name=weight, type=FLOAT, repetitiontype=REQUIRED",
      "Fields": null
    },
    {
      "Tag": "name=sex, type=BOOLEAN, repetitiontype=REQUIRED",
      "Fields": null
    },
    {
      "Tag": "name=day, type=DATE, repetitiontype=REQUIRED",
      "Fields": null
    }
  ]
}

```