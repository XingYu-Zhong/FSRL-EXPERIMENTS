# Multi-Strategy-Reinforcement-Learning-in-Financial-Markets
paper ’Multi-Strategy Reinforcement Learning in Financial Markets‘ Experimental code.

The main difference between him and FSRL is that FSRL is constantly updated, but this program is not.

### 💻 Installation

Firstly, install the Python libraries listed in the `requirements.txt`.

```shell
pip install -r requirements.txt
```
Afterwards, install ta_lib. Make sure to select the appropriate ta_lib installation according to your specific environment.

### 🚀 Quick Start
1.Configure global_config.json in the config directory, mainly to set up your email information and other settings.
2.Register an account on the official Tushare website, retrieve your token, and then configure the commission rate and minimum commission for the backtest system in test_account.json located in the config directory.
3.Configure your data, environment, model, etc. in test_mainlab.json, also located in the config directory.
4.Begin training FSRL.
```shell
python -u run.py --task_name=hDJIADQN\
                 --env_type=train\
                 --start_time=20101201\
                 --end_time=20210101
```
5.After training is completed, test the model.
```shell
python -u run.py --task_name=hDJIADQN\
                 --env_type=test\
                 --start_time=20201201\
                 --end_time=20230101
```

Note:experimentaldata is the data containing the experimentally trained model and test data from the thesis