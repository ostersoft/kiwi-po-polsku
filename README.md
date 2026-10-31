git clone https://github.com/ostersoft/kiwi-po-polsku.git
py -3.12 -m venv venv
venv\Scripts\activate
python -m pip install -r requirements.txt


Invoke-WebRequest `
 -Uri "https://huggingface.co/rhasspy/piper-voices/resolve/main/pl/pl_PL/gosia/medium/pl_PL-gosia-medium.onnx.json" `
 -OutFile ".\piper-models\pl_PL-gosia-medium.onnx.json"`
Invoke-WebRequest `
 -Uri "https://huggingface.co/rhasspy/piper-voices/resolve/main/pl/pl_PL/gosia/medium/pl_PL-gosia-medium.onnx" `
 -OutFile ".\piper-models\pl_PL-gosia-medium.onnx"`

//install openclaw - manual install.

python -m kiwi
openclaw devices list
openclaw devices approve your_id
