<!SLIDE center transition=scrollUp>
# Check Definition

## [How does one look?]

<!SLIDE code medium transition=scrollUp>
    @@@
    {
      "checks": {
        "foo": {
          "command": "echo -n foo && exit 1",
          "subscribers": [
            "bar"
          ],
          "interval": 30
        }
      }
    }

<!SLIDE code medium>
    @@@
    {
      "checks": {
        "foo": {
          "command": "echo -n foo && exit 1",
          "subscribers": [
            "bar"
          ],
          "interval": 30,
          "handlers": ["baz", "qux"],
          "custom": {
            "nested": "attribute"
          }
        }
      }
    }

<!SLIDE code medium>
    @@@
    {
      "checks": {
        "foo": {
          "type": "metric",
          "command": "echo metric 42 `date +%s`",
          "subscribers": [
            "bar"
          ],
          "interval": 10
        }
      }
    }

<!SLIDE code medium>
    @@@
    {
      "checks": {
        "foo": {
          "type": "metric",
          "command": "echo metric 42 `date +%s`",
          "standalone": true,
          "interval": 10
        }
      }
    }
