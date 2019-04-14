# 如何通过时间序列预测项目

> 原文： [https://machinelearningmastery.com/work-time-series-forecast-project/](https://machinelearningmastery.com/work-time-series-forecast-project/)

时间序列预测过程是一组步骤或秘籍，可引导您定义问题，直至具有时间序列预测模型或预测集的结果。

在这篇文章中，您将发现可用于指导您完成预测项目的时间序列预测流程。

阅读这篇文章后，你会知道：

*   Hyndman 和 Athanasopoulos 的 5 步预测任务将指导您从问题定义到使用和评估您的预测模型。
*   Shmueli 和 Lichtendahl 的迭代预测开发流程将指导您将目标定义为实施预测。
*   处理您自己的时间序列预测项目的建议和技巧。

让我们开始吧。

![How to Work Through a Time Series Forecast Project](img/b9cc2dc624f0a6e7e4da7dc2f492d22d.jpg)

如何通过时间序列预测项目
照片由 [TravelingOtter](https://www.flickr.com/photos/travelingotter/1484904858/) ，保留一些权利。

## 5 步预测任务

Hyndman 和 Athanasopoulos 在他们的书[预测：原则和实践](http://www.amazon.com/dp/0987507109?tag=inspiredalgor-20)中总结了预测任务中的 5 个基本步骤。这些步骤是：

1.  **问题定义**。仔细考虑谁需要预测以及如何使用预测。这被描述为该过程中最困难的部分，很可能是因为它完全是问题特定和主观的。
2.  **收集信息**。收集历史数据进行分析和建模。这还包括访问领域专家和收集有助于最好地解释历史信息的信息，以及最终将要进行的预测。
3.  **初步探索性分析**。使用简单的工具（如图形和摘要统计）来更好地理解数据。回顾图并总结并注意明显的时间结构，如趋势季节性，缺失数据，腐败和异常值等异常情况，以及可能影响预测的任何其他结构。
4.  **选择和拟合模型**。评估问题中的两个，三个或一组不同类型的模型。可以基于它们做出的假设以及数据集是否符合来选择模型用于评估。模型已配置并适合历史数据。
5.  **使用和评估预测模型**。该模型用于进行预测，评估这些预测的表现并估算模型的技能。这可能涉及对历史数据进行回溯测试或等待新观察结果可用于比较。

这个 5 个步骤的过程提供了从概念或问题陈述开始到可用于进行预测的模型的强大概述。

该过程的重点是理解问题并拟合一个好的模型。

> 每个模型本身是一个基于一组假设（显式和隐式）的人工构造，并且通常涉及一个或多个必须使用已知历史数据“拟合”的参数。

- 第 22 页，[预测：原则与实践](http://www.amazon.com/dp/0987507109?tag=inspiredalgor-20)

## 迭代预测开发过程

作者 Shmueli 和 Lichtendahl 在他们的书[实用时间序列预测与 R：动手指南](http://www.amazon.com/dp/0997847913?tag=inspiredalgor-20)中提出了一个 8 步骤的过程。

这个过程超出了模型的开发和预测，并涉及迭代循环。

他们的过程可归纳如下：

1.  定义目标。
2.  获取数据。
3.  探索和可视化系列。
4.  预处理数据。
5.  分区系列。
6.  应用预测方法。
7.  评估和比较表现。
8.  实施预测/系统。

以下是流程中的迭代循环：

*   **探索和可视化系列=＆gt;获取数据**。数据探索可能会导致需要访问新数据的问题。
*   **评估和比较表现=＆gt;应用预测方法/** 。对模型的评估可能会为新方法或新方法配置提出问题或想法。

该过程更侧重于对问题的一个或多个模型的持续开发和改进，直到达到可接受的表现水平。

随着新数据和新见解的提供，在修改和更新模型的过程中，此过程可以继续。

> 当然，一旦生成预测，该过程就不会结束，因为预测通常是一个持续的目标。因此，监测预测准确性，并且有时调整或改变预测方法以适应目标或数据随时间的变化

- 第 16 页， [R 实用时间序列预测：动手指南](http://www.amazon.com/dp/0997847913?tag=inspiredalgor-20)

## 建议和提示

本节列出了在完成时间序列预测项目时需要考虑的 10 条建议和提示。

这些建议的主旨集中在这样一个前提，即你无法知道哪些方法可行，更不用说哪种方法可以预先解决你的问题。而预测项目的最佳知识来源是真实历史数据的试错结果。

*   选择或设计适合您的项目，工具，团队和专业水平的时间序列预测流程。
*   写下你在分析和预测工作中所有的假设和问题，然后在以后重新审视它们，并通过对历史数据的小实验来寻求答案。
*   在不同的时间尺度，缩放和观察变换中查看大量的数据图，以帮助使数据中的可利用结构显而易见。
*   使用有意义的表现测量和可靠的测试策略（例如前瞻性验证（滚动预测））开发用于评估模型的强大测试工具。
*   从简单的朴素预测模型开始，为更复杂的方法提供表现基准。
*   为您的时间序列数据创建大量透视图或视图，包括一套自动变换，并使用一个或一组模型评估每个透视图或视图，以帮助自动发现非直观的表示和模型组合，从而获得良好的预测你的问题。
*   从简单到更高级的方法，尝试一系列不同类型的模型来解决您的问题。
*   针对给定问题尝试一套配置，包括在其他问题上运行良好的配置。
*   尝试使用模型的自动超参数优化方法来清除一套表现良好的模型以及您不会手动尝试的非直观模型配置。
*   为正在进行的预测设计表现和技能的自动化测试，以帮助自动确定模型是否以及何时变得陈旧并需要审查或重新训练。

## 进一步阅读

本节列出了一些可用于了解时间序列预测过程的资源。

*   第 1.3 节预测过程，[实际时间序列预测与 R：动手指南](http://www.amazon.com/dp/0997847913?tag=inspiredalgor-20)。
*   第 1.6 节预测任务的基本步骤，[预测：原则和实践](http://www.amazon.com/dp/0987507109?tag=inspiredalgor-20)

你知道有关时间序列预测过程的任何好资源吗？
在下面的评论中分享。

## 摘要

在这篇文章中，您发现了可用于处理时间序列预测问题的流程。

具体来说，你学到了：

*   通过 Hyndman 和 Athanasopoulos 完成时间序列预测任务的 5 个步骤。
*   由 Shmueli 和 Lichtendahl 定义目标和实施预测系统的 8 步迭代过程。
*   在完成时间序列预测项目时需要考虑的 10 条建议和实用技巧。

您对时间序列预测流程或此帖有任何疑问吗？
在下面的评论中提出您的问题。