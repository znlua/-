### 项目经历

**项目名称**: 基于Apple Watch的短期睡眠监测应用（独立开发者）  
**项目时间**: 2021年12月 - 2022年2月

#### 项目描述
该项目主要是设计一款用于短期睡眠的应用程序，能够在用户进入深度睡眠之前将其唤醒。应用程序利用Apple Watch的心率数据来估算用户的睡眠阶段，并根据不同睡眠阶段之间的过渡确定最佳唤醒时间。项目基于一个倒计时应用程序，在倒计时的同时收集用户的心率数据，并估算此时的睡眠阶段。

#### 个人工作
1. **心率数据处理**：通过Apple Watch获取用户的心率数据，并使用平均RRI（心跳间隔）来估算用户的睡眠阶段。
   - 利用公式 \( Ave\_RRI = \frac{60s}{bpm} \) 计算每5秒的平均RRI。
2. **睡眠阶段预测**：参考相关研究，利用心跳的RRI数据通过Lorenz图评估睡眠深度。
   - 计算12个连续1分钟的RRI的中心点和变化量，并推算椭圆面积。
   - 使用最小二乘法进行回归分析，确定睡眠深度的变化趋势。
3. **开发和实现**：使用Swift UI设计应用界面，并基于CircleTimer-main实现倒计时功能。
   - 实现心率数据的实时更新和处理，确保用户在最佳时间被唤醒。

#### 项目难点
1. **数据准确性**：由于Apple Watch只能提供30秒的心电图记录，如何有效利用5秒心率数据估算RRI成为关键。
   - 解决方法：采用平均RRI作为近似值，利用连续数据段进行评估。
2. **睡眠阶段估算**：准确区分不同睡眠阶段是应用的核心难点。
   - 解决方法：参考现有研究，通过Lorenz图的变化趋势和椭圆面积的稳定性评估睡眠深度。
3. **实时处理和响应**：确保心率数据的实时处理和倒计时功能的无缝结合。
   - 解决方法：优化数据处理算法，确保应用的流畅运行和用户体验。

#### 个人收获
1. **技术提升**：在项目开发过程中深入了解了心率数据处理和睡眠阶段预测的相关技术，熟练掌握了Swift UI的应用开发。
2. **问题解决能力**：通过解决项目中的数据处理和算法实现难题，提高了独立分析和解决问题的能力。
3. **项目管理**：作为独立开发者，培养了良好的项目管理能力，能够有效规划和推进项目进程，确保项目按时完成。
