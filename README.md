Blockchain Assessment

👤 Author
Mehul Kaushal (mehulkaushal29)

📌 Project Overview
This project is part of my blockchain assessment.  
It demonstrates a simple blockchain built with Python and Flask.  

The project includes:
- Phase 1: Single node blockchain (transactions + mining)
- Phase 2: Multi-node consensus (3 nodes sync)
- Phase 3: Difficulty experiment (000 / 0000 / 00000)
- Phase 4: Results & analysis

 Requirements
- Python 3.12+
- Flask
- Requests

Install dependencies:
`bash
pip install flask requests


To run: 
git clone https://github.com/mehulkaushal29/blockchain-assessment.git
cd blockchain-assessment

Run 3 nodes: 
python blockchain_assessment.py 5050
python blockchain_assessment.py 5051
python blockchain_assessment.py 5052

Use curl commands:
# Add transaction
curl -X POST http://127.0.0.1:5050/transactions/new \
  -H "Content-Type: application/json" \
  -d '{"sender":"alice","recipient":"bob","amount":5}'

# Mine block
curl http://127.0.0.1:5050/mine

# Sync nodes
curl http://127.0.0.1:5051/nodes/sync

| Difficulty | Tx Add Time (s) | Mining Time (s) | Sync Time (s) | Notes    |
| ---------- | --------------- | --------------- | ------------- | -------- |
| 000        | 0.0004          | 0.0090          | 0.0080        | Easy     |
| 0000       | 0.0005          | 0.0141          | 0.0065        | Baseline |
| 00000      | 0.0004          | 5.4830          | 0.0065        | Hard     |


