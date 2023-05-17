# Azure Policy as code demo

1. Clone repo: `git clone https://github.com/pierskarsenbarg/azure-policy-as-code-demo`
1. Activate virtual environment: `source venv/bin/activate && cd policy && source venv/bin/activate && cd ..`
1. Install packages: `pip3 install -r requirements.txt && cd policy && pip3 install -r requirements.txt && cd ..`
1. Run update with policy: `pulumi up --policy-pack ./policy` - it will fail the policy check
1. Comment out the `public_access` input ([this line](https://github.com/pierskarsenbarg/azure-policy-as-code-demo/blob/2ff1db599e9f8d8786e3b3d3ef39bab0d58ebdb8/__main__.py#L24))
1. Run update with policy: `pulumi up --policy-pack ./policy` - it will pass the policy check
