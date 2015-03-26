## CloudNative Bakery - JSON Webhook examples

Full documentation on how to use this can be found here:

https://cloudnative.io/docs/bakery/json-webhook/

Basically, you can start baking an AMI by sending a POST request to the wehbook URL of a Bakery Build Pipeline.

You can send a request using the `sample.json` file

    curl -X POST --data @sample.json 'https://bakery.cloudnative.com/demo/pipelines/123/hooks/json/s0m3CODEh3r3.json'

(the exact URL will be on the details page of your Build Pipeline)

Any questions or comments, please:

[![Join the chat at https://gitter.im/cloudnative/bakery-examples](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/cloudnative/bakery-examples?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
