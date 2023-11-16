---
description: Commonly used Command Line Interface (CLI) scripts
---

# Other Useful Commands

## Get versions

```bash
agd version
```

Sample Result

```
0.35.0-u11.0
```

## Get verbose versions

```bash
agd  version --long
```

Sample Result

{% code fullWidth="false" %}
```bash
name: agoriccosmos
server_name: agd
version: 0.35.0-u11.0
commit: 92b6cd724
build_tags: ledger
go: go version go1.20.8 linux/amd64
build_deps:
- filippo.io/edwards25519@v1.0.0-beta.2
- github.com/99designs/keyring@v1.1.6 => github.com/cosmos/keyring@v1.1.7-0.20210622111912-ef00f8ac3d76
- github.com/ChainSafe/go-schnorrkel@v0.0.0-20200405005733-88cbf1b4c40d
- github.com/Workiva/go-datastructures@v1.0.53
- github.com/armon/go-metrics@v0.4.0
- github.com/beorn7/perks@v1.0.1
- github.com/bgentry/speakeasy@v0.1.0
- github.com/btcsuite/btcd@v0.22.1
- github.com/cespare/xxhash/v2@v2.1.2
- github.com/coinbase/rosetta-sdk-go@v0.7.0
- github.com/confio/ics23/go@v0.7.0 => github.com/agoric-labs/cosmos-sdk/ics23/go@v0.8.0-alpha.agoric.1
- github.com/cosmos/btcutil@v1.0.4
- github.com/cosmos/cosmos-sdk@v0.45.11 => github.com/agoric-labs/cosmos-sdk@v0.45.11-alpha.agoric.3
- github.com/cosmos/go-bip39@v1.0.0
- github.com/cosmos/iavl@v0.19.4
- github.com/cosmos/ibc-go/v3@v3.4.0
- github.com/cosmos/ledger-cosmos-go@v0.11.1
- github.com/cosmos/ledger-go@v0.9.2
- github.com/creachadair/taskgroup@v0.3.2
- github.com/davecgh/go-spew@v1.1.1
- github.com/desertbit/timer@v0.0.0-20180107155436-c41aec40b27f
- github.com/dvsekhvalnov/jose2go@v0.0.0-20200901110807-248326c1351b
- github.com/felixge/httpsnoop@v1.0.2
- github.com/fsnotify/fsnotify@v1.5.4
- github.com/go-kit/kit@v0.12.0
- github.com/go-kit/log@v0.2.1
- github.com/go-logfmt/logfmt@v0.5.1
- github.com/godbus/dbus@v0.0.0-20190726142602-4481cbc300e2
- github.com/gogo/gateway@v1.1.0
- github.com/gogo/protobuf@v1.3.3 => github.com/regen-network/protobuf@v1.3.3-alpha.regen.1
- github.com/golang/protobuf@v1.5.2
- github.com/golang/snappy@v0.0.4
- github.com/google/btree@v1.0.1
- github.com/google/orderedcode@v0.0.1
- github.com/gorilla/handlers@v1.5.1
- github.com/gorilla/mux@v1.8.0
- github.com/gorilla/websocket@v1.5.0
- github.com/grpc-ecosystem/go-grpc-middleware@v1.3.0
- github.com/grpc-ecosystem/grpc-gateway@v1.16.0
- github.com/gsterjov/go-libsecret@v0.0.0-20161001094733-a6f4afe4910c
- github.com/gtank/merlin@v0.1.1
- github.com/gtank/ristretto255@v0.1.2
- github.com/hashicorp/go-immutable-radix@v1.3.1
- github.com/hashicorp/golang-lru@v0.5.4
- github.com/hashicorp/hcl@v1.0.0
- github.com/hdevalence/ed25519consensus@v0.0.0-20210204194344-59a8610d2b87
- github.com/improbable-eng/grpc-web@v0.14.1
- github.com/klauspost/compress@v1.15.11
- github.com/lib/pq@v1.10.6
- github.com/libp2p/go-buffer-pool@v0.1.0
- github.com/magiconair/properties@v1.8.6
- github.com/mattn/go-colorable@v0.1.13
- github.com/mattn/go-isatty@v0.0.16
- github.com/matttproud/golang_protobuf_extensions@v1.0.2-0.20181231171920-c182affec369
- github.com/mimoo/StrobeGo@v0.0.0-20210601165009-122bf33a46e0
- github.com/minio/highwayhash@v1.0.2
- github.com/mitchellh/mapstructure@v1.5.0
- github.com/mtibben/percent@v0.2.1
- github.com/pelletier/go-toml/v2@v2.0.5
- github.com/pkg/errors@v0.9.1
- github.com/pmezard/go-difflib@v1.0.0
- github.com/prometheus/client_golang@v1.12.2
- github.com/prometheus/client_model@v0.2.0
- github.com/prometheus/common@v0.34.0
- github.com/prometheus/procfs@v0.8.0
- github.com/rakyll/statik@v0.1.7
- github.com/rcrowley/go-metrics@v0.0.0-20201227073835-cf1acfcdf475
- github.com/regen-network/cosmos-proto@v0.3.1
- github.com/rs/cors@v1.8.2
- github.com/rs/zerolog@v1.27.0
- github.com/spf13/afero@v1.8.2
- github.com/spf13/cast@v1.5.0
- github.com/spf13/cobra@v1.6.0
- github.com/spf13/jwalterweatherman@v1.1.0
- github.com/spf13/pflag@v1.0.5
- github.com/spf13/viper@v1.13.0
- github.com/stretchr/testify@v1.8.0
- github.com/subosito/gotenv@v1.4.1
- github.com/syndtr/goleveldb@v1.0.1-0.20210819022825-2ae1ddf74ef7
- github.com/tendermint/btcd@v0.1.1
- github.com/tendermint/crypto@v0.0.0-20191022145703-50d29ede1e15
- github.com/tendermint/go-amino@v0.16.0
- github.com/tendermint/tendermint@v0.34.23 => github.com/agoric-labs/tendermint@v0.34.23-alpha.agoric.3
- github.com/tendermint/tm-db@v0.6.7
- github.com/zondax/hid@v0.9.0 => github.com/zondax/hid@v0.9.1-0.20220302062450-5552068d2266
- golang.org/x/crypto@v0.1.0
- golang.org/x/exp@v0.0.0-20220722155223-a9213eeb770e
- golang.org/x/net@v0.7.0
- golang.org/x/sys@v0.5.0
- golang.org/x/term@v0.5.0
- golang.org/x/text@v0.7.0
- google.golang.org/genproto@v0.0.0-20221014213838-99cd37c6964a
- google.golang.org/grpc@v1.50.1 => google.golang.org/grpc@v1.33.2
- google.golang.org/protobuf@v1.28.2-0.20220831092852-f930b1dc76e8
- gopkg.in/ini.v1@v1.67.0
- gopkg.in/yaml.v2@v2.4.0
- gopkg.in/yaml.v3@v3.0.1
- nhooyr.io/websocket@v1.8.6
cosmos_sdk_version: v0.45.11
```
{% endcode %}

## Check Status

```bash
curl 127.0.0.1:14457/status
```

Sample Result

```json
{
  "jsonrpc": "2.0",
  "id": -1,
  "result": {
    "node_info": {
      "protocol_version": {
        "p2p": "8",
        "block": "11",
        "app": "0"
      },
      "id": "c1dc9...79475",
      "listen_addr": "[YOUR IP]:14456",
      "network": "agoric-emerynet-8",
      "version": "0.34.23",
      "channels": "40202122233038606100",
      "moniker": "test-agoric-main",
      "other": {
        "tx_index": "off",
        "rpc_address": "tcp://0.0.0.0:14457"
      }
    },
    "sync_info": {
      "latest_block_hash": "3F63FE8700D15ACB46612931AD9B3DA40270B0A379A17462059207A813D6645D",
      "latest_app_hash": "C015C46B7AFFA73145FC7D3E55383B2DFF9833556B5075AC99C1E3843CB9474C",
      "latest_block_height": "1593488",
      "latest_block_time": "2023-09-20T13:46:01.199410173Z",
      "earliest_block_hash": "88977C1347A93816EEFCE8631C92A4C4D712F133B0EDA352382304F3E9E9CED4",
      "earliest_app_hash": "A2233ED992002D5937FAC5297EF0B2BE1888BAB2D1FE5EACCE0059865ED3AFBD",
      "earliest_block_height": "1561001",
      "earliest_block_time": "2023-09-18T10:46:48.032799174Z",
      "catching_up": false
    },
    "validator_info": {
      "address": "1BC85D8C37872D47B99011E4EE321FE74E99CE40",
      "pub_key": {
        "type": "tendermint/PubKeyEd25519",
        "value": "mf7zJ6VZOe6Rryf/hUnLa/pS9vLJS+zAZzM63W1xNqE="
      },
      "voting_power": "0"
    }
  }
}
```

### Alternate command

```bash
agd status --node tcp://127.0.0.1:14457
```

Sample Result

```json
{"NodeInfo":{"protocol_version":{"p2p":"8","block":"11","app":"0"},"id":"c1dc9...79475","listen_addr":"[YOUR IP]:14456","network":"agoric-emerynet-8","version":"0.34.23","channels":"40202122233038606100","moniker":"test-agoric-main","other":{"tx_index":"off","rpc_address":"tcp://0.0.0.0:14457"}},"SyncInfo":{"latest_block_hash":"2FDBBEBAC19CACD31B37B1480949658DBA2FC668EE1F594EFB573FC6A0DF8D47","latest_app_hash":"82A84446E478F94296C5CB6B2FAC55D77F372F991246E6081E2EE7E845B81392","latest_block_height":"1593541","latest_block_time":"2023-09-20T13:50:59.984302065Z","earliest_block_hash":"88977C1347A93816EEFCE8631C92A4C4D712F133B0EDA352382304F3E9E9CED4","earliest_app_hash":"A2233ED992002D5937FAC5297EF0B2BE1888BAB2D1FE5EACCE0059865ED3AFBD","earliest_block_height":"1561001","earliest_block_time":"2023-09-18T10:46:48.032799174Z","catching_up":false},"ValidatorInfo":{"Address":"D8C37.....FE74E","PubKey":{"type":"tendermint/PubKeyEd25519","value":"ryf9v.....="},"VotingPower":"0"}}
```



## Get blocks

```bash
curl 127.0.0.1:14457/block
```

Sample Result

```json
{
  "jsonrpc": "2.0",
  "id": -1,
  "result": {
    "block_id": {
      "hash": "5517185459DEBC6DF23036633880CDBBA3D0C7BE98CB790998A1044837FC57FD",
      "parts": {
        "total": 1,
        "hash": "C6BE9FDE049965BA497A5528A27C1111083463D4EFD5DD1948BA2DE870863E1F"
      }
    },
    "block": {
      "header": {
        "version": {
          "block": "11"
        },
        "chain_id": "agoric-emerynet-8",
        "height": "1593572",
        "time": "2023-09-20T13:53:54.757278946Z",
        "last_block_id": {
          "hash": "F6467A2C8FF8A03FB6AD816CD3B245B3CA4C0B596CC6976A64171165423A27F3",
          "parts": {
            "total": 1,
            "hash": "532E25A50F0C597E6E6999E1194B548B1D4CC2DBAEA5F01BFCC683B550945F01"
          }
        },
        "last_commit_hash": "F4C457FD41CE675E8A8B637371F18801F1B5BC310F5036ABA22ADE6E7DA5DC4B",
        "data_hash": "E3B0C44298FC1C149AFBF4C8996FB92427AE41E4649B934CA495991B7852B855",
        "validators_hash": "562C689D73C5E3A7B0A99837C2ACDD2022724550309D37689F604239C084BA37",
        "next_validators_hash": "562C689D73C5E3A7B0A99837C2ACDD2022724550309D37689F604239C084BA37",
        "consensus_hash": "048091BC7DDC283F77BFBF91D73C44DA58C3DF8A9CBC867405D8B7F3DAADA22F",
        "app_hash": "DD4AC43F5788C9925DDF2DD03EACBAC8FD365AF193D8196471562D2618FBFDB9",
        "last_results_hash": "E3B0C44298FC1C149AFBF4C8996FB92427AE41E4649B934CA495991B7852B855",
        "evidence_hash": "E3B0C44298FC1C149AFBF4C8996FB92427AE41E4649B934CA495991B7852B855",
        "proposer_address": "F7A60CFAD351A7BA96B19EC9852EC56158C7DB9E"
      },
      "data": {
        "txs": []
      },
      "evidence": {
        "evidence": []
      },
      "last_commit": {
        "height": "1593571",
        "round": 0,
        "block_id": {
          "hash": "F6467A2C8FF8A03FB6AD816CD3B245B3CA4C0B596CC6976A64171165423A27F3",
          "parts": {
            "total": 1,
            "hash": "532E25A50F0C597E6E6999E1194B548B1D4CC2DBAEA5F01BFCC683B550945F01"
          }
        },
        "signatures": [
          {
            "block_id_flag": 2,
            "validator_address": "1E1B939E6D3CCFC7FD2F832A837BEEC5507C0BA4",
            "timestamp": "2023-09-20T13:53:54.707731802Z",
            "signature": "IMtUVu7AQGcppQgnO/LsvQZda2Xa2w91OsazYwHZgfTTSs7VLu6UETCU5Sdi0wHjyC2L4bvMpCHHhSnuvH4aBQ=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "BC086C7F34A3361CB75F07A882E6A7751C6E1DA8",
            "timestamp": "2023-09-20T13:53:54.761948725Z",
            "signature": "5yeugdn6bRqbHUu85iRHSCTaXWZe/IaD2IRHY1i6LDPzdaToZwzXwqGXJM81DxPiLKpUWcxktFrrPcwfHsR/AA=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "61D286818CD671A60767040E8167724183E575EA",
            "timestamp": "2023-09-20T13:53:54.811383357Z",
            "signature": "+uo2hSKe12WLuSRxa8kTHnbYyRSJySk2gZVVFwgOQEk3b/+9tYYhfiRQcatCnI7XI6rcIoe73V5rPAPA4lx1Aw=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "D881537CD07CB0383645F44CAA8D7D67E1E32CEA",
            "timestamp": "2023-09-20T13:53:54.757278946Z",
            "signature": "4Ckiq4O05v/922IzH5A9CiH3fH2ej78QBgSyAnnix+X24KViSLwp+njrl3KaGSRJfc6jG5VL7qs0FoT7d5G9AA=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "3B8515F62E2D6B6A2EC65B47B302800AA9F2687B",
            "timestamp": "2023-09-20T13:53:54.757120554Z",
            "signature": "4933OvOOOWKSN8qsmuC2MXZbhVyXzGw9Z+uPpHCpcQdxIQe+M4bNkIdH1984R3lZUiLDJg9Nn5biEgwzWOHqAA=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "D9C01AE1781B5058DA209E75C3E163042FE92D95",
            "timestamp": "2023-09-20T13:53:54.764057653Z",
            "signature": "WliMYK8UgxSDMOu7/6sSIrO91cO6m/TKyHSoVjvdEtPu6+qgWsvhostHBO5Q0guNYOLGiq56LYrSMlM0YjHvBA=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "FECC261776772111BA28A274452E2890E6DC11E9",
            "timestamp": "2023-09-20T13:53:54.767356668Z",
            "signature": "yulIvPWVWXp7LNuVfnOy5dCGCVr1EoHmfo6k74tBulKJZgkv5suvmjf2e8advfIya/DfzGcdtqA25s4iA3ZvAg=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "702A308B424D3EA957B5033FA804CE1F3B5DA65B",
            "timestamp": "2023-09-20T13:53:54.692037796Z",
            "signature": "xHyn4V4hutWGfxidZaJGVgesUwnuUoPcQXk6d7tsxkrkHTYh5Ks7+60LotNZsbKvnXs0OLnSmTRg8GvTttrTAw=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "F7A60CFAD351A7BA96B19EC9852EC56158C7DB9E",
            "timestamp": "2023-09-20T13:53:54.700243422Z",
            "signature": "AewisZPB4Y/1QU6MBSJe0/4cMy5DHob1KaiWfvIeOHFEVuRo54Ceo5wHiUBsIeBB7vPLLUGvo4xxZKVb7sqmAQ=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "44D286E368B0C5A31859933048748F9ED470EB43",
            "timestamp": "2023-09-20T13:53:54.762645467Z",
            "signature": "rbNaX9USil2w3q5lg5WtVDjuQOuNQckHMznjBxKyPNSq7sIUF0lKPa61UWVZtK46VQthEzjlc1BOLRJEDnWIAw=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "0308A6C41EE7379790C9C1109FE994DF5CBA64D8",
            "timestamp": "2023-09-20T13:53:54.672654831Z",
            "signature": "ZFynkxAb8qlbTWb5Q02qPV2EHsitweqr3jr3Pu/w4AFcbQyoCqLvGK3jv2w6zaSdF6MkWyxLEexpkXAnGIkiBg=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "B5835B919A83A689D47A9BB2146359C0E74F59E3",
            "timestamp": "2023-09-20T13:53:54.695710515Z",
            "signature": "ZBfcfuCS/7lbsOyZnEb+6Kp409bKA9iogkWr6+fNJ7RzjjbSLRLx5902pta7sUvt3SorV1s7zSbfIz+PfglhAQ=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "2568CC579BDF51F750054294D73524E41E922F5E",
            "timestamp": "2023-09-20T13:53:54.710460987Z",
            "signature": "NELagNFWYQYgu3tuDAk1Qa13PEDXMJfZCy45F6WxE684SHnkOpEpQTcOj7S6UgJyv8xHw0XYiWGQ3w/geeazBQ=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "7B886A33C4EFCEE08E178A3D8DC7D5FA0DAF6962",
            "timestamp": "2023-09-20T13:53:54.750807509Z",
            "signature": "9aUp6B7Ow96TUC16BRnmwI8ZqzoQSV4N9d5aInl6V1FmfL60WNxaADbUOKbg9mU0lgNrK6CvShXFiPu6MmEuBw=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "48E2B3E17D81A4EC7D9C46C74BC23969A0B2EED7",
            "timestamp": "2023-09-20T13:53:54.757326127Z",
            "signature": "JATYvbO3d65LAm4HdwTzWU3KegWWz1+v8PM0Rv1B2E519cNvRIm8X5U0aYio+vcHxyM5zfXTPAVKOFrxuBSvAw=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "8B1C388FCB7C55286384648597F3282AE9F78DF8",
            "timestamp": "2023-09-20T13:53:54.756357379Z",
            "signature": "jYsJartEo6FVgTgYoOoN5ItASSesfbmaebmBX7ZRcEcVZSMfrdPC8MYwtZIgz0qOOaMDoELrzadktVmGACZLBQ=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "EFE53120F79431764A1ED2CEF83376777AE39F72",
            "timestamp": "2023-09-20T13:53:54.670612355Z",
            "signature": "67B6z+EgWOrNB3qqIQsyv9zIG9Pe3fl/r5+d7RlplAGRIaqzfZa6rnrBwWhhGuY4JidnaNyXY3QvxIl/ulYzDw=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "C9FBAB74B9902E404996420CC7A3A77F1E77AF2A",
            "timestamp": "2023-09-20T13:53:54.75908408Z",
            "signature": "NUnYNVWTR+ewyo9uChFdlsQXO6n996H6Wwo4txMOxScxMUOvVkkEhSNfybeqRLE0106V0Zba0IcIbeHOnvwpAA=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "ED1B3F31A99CD520C565DDB6A88405A388B7984F",
            "timestamp": "2023-09-20T13:53:54.683925215Z",
            "signature": "x9dL9W4bSii5mHqfD+CVzF8nE8W924k/DS1Ob/HPBK2z24v5KbEohwGniVm1/LJ1jU6C29anASWy2rr807MiAQ=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "DC9901FAEF22ECEA45B6A4CF5BDAA2DB5D458B18",
            "timestamp": "2023-09-20T13:53:54.67625943Z",
            "signature": "RMaejS2V90p9qJVg6ou7S0h9WCvOzdG96wP99ZGz1o/y4ml32JQQSQ48d6fXHsqTb8ZVTgQ+CDiiD7yE6yN+Cg=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "0EB137A895EC55B7C0BD1CBF2743DB3BD6FAB497",
            "timestamp": "2023-09-20T13:53:54.852257213Z",
            "signature": "IZfR8w8Qx+RsUy0x3DVjAJaW6bdfds+NRuGHWpGqmBHMqvHPqhRpasmQ9JojYG780hANKyXexPFYv7naw/ryDg=="
          },
          {
            "block_id_flag": 2,
            "validator_address": "969B20BC44DC432D55C051054A0E91CD2B0842A6",
            "timestamp": "2023-09-20T13:53:54.747491699Z",
            "signature": "BJLEm+yGdiKD3duAGeBkQmrzWdxagtFfzbEaJBG4cLmUAkzlpVZzJD71YlCfObX5k604nw6Y/Tx9sP/5gXlXCg=="
          }
        ]
      }
    }
  }
}
```

## Get block height

```bash
curl  -s 127.0.0.1:14457/block  | jq -r .result.block.header.height
```

Sample Result

```
1593586
```

## Count Connected Peers

To look for number of peers

```json
curl  -s 127.0.0.1:14457/net_info  | jq .result.n_peers
```

Sample Results

```
"17"
```

## Connected Peers IP addresses

```bash
curl  -s 127.0.0.1:14457/net_info | jq .result.peers | grep remote
```

Sample Results

```bash
    "remote_ip": "63.229.234.75"
    "remote_ip": "38.242.156.28"
    "remote_ip": "95.214.54.27"
    "remote_ip": "141.94.138.48"
    "remote_ip": "208.88.251.50"
    "remote_ip": "5.9.81.187"
    "remote_ip": "70.58.17.174"
    "remote_ip": "195.201.108.152"
    "remote_ip": "178.23.126.84"
    "remote_ip": "54.203.15.32"
    "remote_ip": "65.109.23.238"
    "remote_ip": "65.109.23.114"
    "remote_ip": "34.171.162.87"
    "remote_ip": "65.108.226.183"
    "remote_ip": "38.109.200.33"
    "remote_ip": "65.109.68.190"
    "remote_ip": "116.202.231.58"
```

## Check Consensus State

```
curl  -s 127.0.0.1:14457/consensus_state \
  | jq '.result.round_state.height_vote_set[0].prevotes_bit_array'
```

Sample Results

```json
"BA{22:______________________} 0/3007 = 0.00"
```

## Pre-vote

```bash
curl localhost:26657/consensus_state \
  | jq '.result.round_state.height_vote_set[0].prevotes[]' \
  | grep 'Vote{' \
  | grep <first 6 characters of validator address>
```
