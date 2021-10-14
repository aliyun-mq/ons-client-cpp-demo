# ons-client-cpp-demo

## How to build
```bash
bazel build //examples/...
```

## How to run
1. Make sure you have modified examples, replacing placeholder access key/secret, access-point, group-id with your actual values;
2. Run examples with the following commands.
   1. Let's send some messages first
    ```bash
    bazel run //examples:example_producer
    ```

   2. To consume these messages, 
   ```bash
   bazel run //examples:example_push_consumer
   ``` 