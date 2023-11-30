Role Name
=========

ansible-vllm

Requirements
------------

None, currently.

Role Variables
--------------

|| Name || Default || Description ||
| VLLM_MODEL | None | The path to the model file, e.g. lmsys/vicuna-7b-v1.5 |
| VLLM_MAX_NUM_BATCHED_TOKENS | 8192 | The maximum number of tokens to batch together |
| VLLM_MAX_MODEL_LENGTH | 8192 | The maximum length of the model |
| VLLM_API_SERVER_ENABLE | true | Whether to enable the API server |
| VLLM_API_SERVER_LOCAL_ONLY | false | Whether to only listen on localhost |
| VLLM_API_SERVER_HOST | 0.0.0.0 | The host to listen on (0.0.0.0 = listen on any address, 127.0.0.1 listen on localhost only) |
| VLLM_API_SERVER_PORT | 8000 | The port to listen on |
| VLLM_TENSOR_PARALLEL_SIZE | 1 | The number of GPUs to use for tensor parallelism; you can increase if using distributed compute |

Dependencies
------------

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      tasks:
        - ansible.builtin.import_role: 
            name: ansible-vllm

License
-------

BSD

Author Information
------------------

Edwin Skidmore (edwins@arizona.edu)
