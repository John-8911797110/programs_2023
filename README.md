# Programs_2023
describe programs simply

## CTA strategy development

- #### Object modules 

  1. Updater: update daily data from Wind.
  2. Combiner: dataloader and combiner near month data or other style data.
  3. indicator: receive data and generate signal.
  4. Account: trading, settling and save backtest performance.

- #### Backtest

  1. single strategy: develop atrma, ts, mmt...
  2. achieve contract change month, sector margin limitation...
  3. scenario analysis for strategies.
  4. visualization

  **[visualization example](asset/all.html)**

  <img src="asset\multi_strategy_result.png" style="zoom:100%;" />
  <img src="asset\multi_strategy_metrics.png" alt="image-20230307142906788"  />



## CSI300 volatility forecast

- #### Data process

  1. select N stock from CSI300 index and process stock tick data into 5min volatility.
  2. window slide to split train/test and transfer train/test dataset S times like 1-4 month for train, 5-6 month for test.
  3. stack different stock data into (N, T, D) dim to train and test.

- #### Transfer learning

  1. build model for train, like(LSTM/GRU + MLP)
  2. pre train model in train/test dataset with Focal Loss、RMSprop...
  3. finetune model in transfer dataset.

<<<<<<< HEAD
  <img src="asset\vol_testacc.png" alt="image-20230307144840116" style="zoom:67%;" />

- #### Simple backtest

  1.  train model in 3-6, 2022, test on 7,1,2022-9,1,2023 (44 trade day).
  2.  allow long and short N in 510300 with fee, covering all positions at 14:50.
  3.  daily return in 8.1-9.1 and 7.1-9.1 result shows below :

<<<<<<< HEAD
  ![image-20230309112851032](asset\backtest_result_example.png)![image-20230309112851032](asset\backtest_result_all.png)
  
  
=======
 <img src="asset\backtest_result_example.png" alt="image-20230309111411371" style="zoom:100%;" />

>>>>>>> add4bb67496b5499cacfd15998b033b7f30ceab2
