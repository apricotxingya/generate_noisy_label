# PEER Module

## download PEER
```shell script
git clone https://github.com/apricotxingya/peer_loss.git
```

## prepare data
- generate *fixed feature vector* by BERT  
```shell script
git clone https://github.com/google-research/bert
```
- download pre-trained model for both English and Chinese
```shell script
cd bert
wget https://storage.googleapis.com/bert_models/2018_10_18/uncased_L-12_H-768_A-12.zip
wget https://storage.googleapis.com/bert_models/2018_11_03/chinese_L-12_H-768_A-12.zip
unzip uncased_L-12_H-768_A-12.zip
unzip chinese_L-12_H-768_A-12.zip
```

- generate PEER format dataset by
```shell script
git clone https://github.com/maopademiao/generate_noisy_label.git
cp ./generate_noisy_label/peer_process/get_data_for_peer.sh
sh get_data_for_peer.sh
sh generate_all_noisy_data_for_PEER.sh
```

## run PEER