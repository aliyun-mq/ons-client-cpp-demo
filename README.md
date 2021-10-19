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

   3. To run other examples, figure out names of targets in [BUILD.bazel](examples/BUILD.bazel), aka, name of the cc_binary, then execute them as the previous two.