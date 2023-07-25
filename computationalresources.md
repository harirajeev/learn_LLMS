<b>you must know these three things:</b>

  - The model size.
  - Details about the hardware to be used.
  - Right inference option.

Once you have the details, you can actually calculate how much-accelerated computing power you need. Based upon that, you can plan and execute your model deployment. 

<b>Calculating model size</b>

 - [Estimating training compute of Deep Learning models](https://www.lesswrong.com/posts/HvqQm6o8KnwxbdmhZ/estimating-training-compute-of-deep-learning-models)
 - [Full doc](https://docs.google.com/document/d/1J2BX9jkE5nN5EA1zYRN0lHhdCf1YkiFERc_nwiYqCOA/edit)
 - [How to measure FLOP/s for Neural Networks empirically?](https://www.lesswrong.com/posts/jJApGWG95495pYM7C/how-to-measure-flop-s-for-neural-networks-empirically)
 - [ a public spreadsheet with some info on different hardware](https://docs.google.com/spreadsheets/d/1AAIebjNsnJj_uKALHbXNfn3_YsT6sHXtCU0q7OIPuc4/edit#gid=0)
 - [Deep Learning GPU Benchmarks](https://lambdalabs.com/gpu-benchmarks)
 - 

You can see the table below, which will give you an idea of how many FLOPs you might need for your model. Once you have an estimation, you can then go ahead and find the relevant GPU in your preferred cloud platform. 

![Uploading image.png…]()

- [Comparing custom ML hardware - MLPerf Benchmarks ](https://mlcommons.org/en/training-normal-11/)
- [MLPerf benchmark paper](https://arxiv.org/pdf/1910.01500.pdf)
