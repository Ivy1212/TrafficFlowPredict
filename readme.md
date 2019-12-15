### 交通流预测

LSTM，GRU，SAEs

#### 实验环境：

- python 3.6
- keras 
- scikit-learn
- Tensorflow 



#### 训练模型

- 首先利用训练模型训练数据，然后利用得到的模型来预测测试数据
- 查看测试数据的结果（MSE）



#### 步骤

- ```python
  python train.py --model model_name
  # model_name 可以指定lstm，gru，SAEs,默认为lstm 
  ```

- ```python
  python train.py 
  ```

  

#### 程序结构

- data/data.py    --进行数据预处理，包括数据切分，数据最大最小化处理
- model/model.py   --LSTM ，gru，SAEs的网络结构设定
- 主目录下的train.py  -- 利用data.py处理后的数据，进一步调用model.py进行模型训练，训练的loss保存在model目录下，并将训练后的模型结果保存在model目录下（.h5格式）
- 利用已经训练好的模型（.h5）对测试数据进行验证



#### 参考文献：

```
@article{SAEs,  
  title={Traffic Flow Prediction With Big Data: A Deep Learning Approach},  
  author={Y Lv, Y Duan, W Kang, Z Li, FY Wang},
  journal={IEEE Transactions on Intelligent Transportation Systems, 2015, 16(2):865-873},
  year={2015}
}

@article{RNN,  
  title={Using LSTM and GRU neural network methods for traffic flow prediction},  
  author={R Fu, Z Zhang, L Li},
  journal={Chinese Association of Automation, 2017:324-328},
  year={2017}
}
```