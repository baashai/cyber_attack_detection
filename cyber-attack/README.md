# **Innovative Approaches to Multivariate Time Series Anomaly Detection: Hybrid Positional Encoding-Based Transformer**

This repository supports our research titled **"Innovative Approaches to Multivariate Time Series Anomaly Detection: Hybrid Positional Encoding-Based Transformer."** It provides a **revamped version** of the original code used to generate the results in our paper, making it more accessible and easier to use.

### **Objective**
This repository is specifically designed to **detect cyber attacks** in multivariate time series data using a **Hybrid Positional Encoding-Based Transformer**. The following steps will help you set up the environment and replicate the results.

---

## **Installation**
This code requires **Python 3.7 or higher**.

To install dependencies, run the following commands:

```bash
pip3 install torch==1.8.1+cpu torchvision==0.9.1+cpu torchaudio===0.8.1 -f https://download.pytorch.org/whl/torch_stable.html
pip3 install -r requirements.txt
```

### **Manual Fix for PyTorch Transformer Module**
Navigate to:
```bash
/usr/local/lib/python3.10/dist-packages/torch/nn/modules/transformer.py
```
At **line 387**, remove the argument **`is_causal = is_causal`**.

Modify the line as follows:
```python
output = mod(output, src_mask=mask, src_key_padding_mask=src_key_padding_mask_for_layers)
```

---

## **Data Preprocessing**
To preprocess the data, run:

```bash
python preprocess.py --dataset <dataset>
```

Here, `<dataset>` can be either of the following:

- **SWaT** (Secure Water Treatment dataset)
- **WADI** (Water Distribution dataset)

Both datasets focus on **cyber attack detection** in critical infrastructure systems.

---

This repository simplifies the implementation and provides a streamlined approach to anomaly detection in **industrial control systems**. Follow the methods outlined above to replicate the results. 🚀

