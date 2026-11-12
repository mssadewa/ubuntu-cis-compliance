# Expected Project Structure

cis-ubuntu-compliance/
│
├── README.md
├── ansible.cfg
│
├── playbooks/
│ └── cis_runner.yml
│
├── benchmarks/
│ │
│ ├── ubuntu_2204_v3/
│ │ ├── benchmark.yml
│ │ ├── catalog.yml
│ │ └── controls/
│ │ ├── section_1
│ │ │ ├── 1.1.1.1.yml
│ │ │ └── ...
│ │ ├── section_2
│ │ │ ├── 2.1.1.1.yml
│ │ │ └── ...
│ │ └── ...
│ │
│ └── ubuntu_2404_v2/
│ ├── benchmark.yml
│ ├── catalog.yml
│ └── controls/
│ │ ├── section_1
│ │ │ ├── 1.1.1.1.yml
│ │ │ └── ...
│ │ ├── section_2
│ │ │ ├── 2.1.1.1.yml
│ │ │ └── ...
│ │ └── ...
│
├── roles/
│ ├── cis_engine/
│ │ └── tasks/
│ │ ├── main.yml
│ │ ├── validate_inputs.yml
│ │ ├── load_catalog.yml
│ │ ├── select_controls.yml
│ │ ├── validate_exceptions.yml
│ │ ├── execute_controls.yml
│ │ └── finalize_results.yml
│ │
│ └── cis_reporting/
│ └── tasks/
│ └── main.yml
│
├── exceptions/
│ ├── ubuntu_2204.yml
│ └── ubuntu_2404.yml
│
└── group_vars/
├── ubuntu_2204.yml
└── ubuntu_2404.yml
