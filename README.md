## Federated Learning with Websockets
Federated training via three websocket connections.
Start_websocket_servers.py will start the Websocket server workers for Alice, Bob and Charlie.
The training is then started by running the script run_websocket_client.py.



This script loads the MNIST dataset,
distributes it onto the three workers
starts a federated training.
The federated training loop contains the following steps
The current model is sent to the workers
The workers train on a fixed number of batches
The three models from Alice, Bob and Charlie are then averaged (federated averaging)
This training loop is then executed for a given number of epochs. The performance on the test set of MNIST is shown after each epoch.
