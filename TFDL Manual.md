# TFDL Manual

* [RNN](#rnn)
* [UFCNN](#ufcnn)
* [ARIMA](#arima)
* [GARCH](#garch)
* [Prophet](#prophet)

## RNN

###### 1. How To Run

###### a) predict

in `predict.py`, run

```python
predict(data_path, 'rnn', params)
```

###### b) training with BO

run with BO tuning, run

```python
params['optimiser'] = 'BO'
predict(data_path, 'rnn', params)
```

###### c) data preparation

tfdl.data_builder` provides convinient tools for data building.

For text segmentation task, use `tfdl.data_builder.binary_text_segmentation`

For sentence classification task, use

`tfdl.data_builder.sentence_classification`

For word tagging task, use

`tfdl.data_builder.text_tagging`

For time series data, use

`tfdl.data_builder.local_delay_embedding`

You can find usage example under `/tfdl/examples/

###### 2. Tunable Parameters

Substite the following parameters into BO for optimisation purpose

```python
params = {
  'learning_rate': (0.05, 1),
  'dropout_keep_prob': (0.5, 1),
  'batch_size': (1, 10),
  'num_of_layers': (1, 11),
  'look_back_steps_n': (10, 20)
}
```

###### 3. Suitable Cases

RNN is suitable for sequential data. Such as image, audio, natural language, time-series data. With right data building and parameters, you should be able to archieve great results.

## UFCNN

###### 1. How To Run

###### 2. Tunable Parameters

###### 3. Suitable Cases



## ARIMA

###### 1. How To Run

###### 2. Tunable Parameters

###### 3. Suitable Cases

## GARCH

###### 1. How To Run

###### 2. Tunable Parameters

###### 3. Suitable Cases

## Prophet

###### 1. How To Run

###### 2. Tunable Parameters

###### 3. Suitable Cases





