📋参数解释：
 PVA_MW PVA分子量（Da） 
 PVA_DH 水解度（%） 
 PVA_Conc PVA浓度（wt%） 
 FC 冻融循环次数 
 CLM 交联方法（编码为0–5） 
 CC 导电填料含量（wt%） 
 硼砂 是否使用硼砂交联 
 EG 是否使用乙二醇 
 GL 是否使用戊二醛 
 MBA 是否使用MBA交联 
 PBA 是否使用聚硼酸 
 AgNPs 是否含银纳米颗粒 
 CNF 是否含碳纳米纤维 
 CNT 是否含碳纳米管 
 LDH 是否含层状双氢氧化物 
 PANI 是否含聚苯胺 
 PEDOT:PSS 是否含PEDOT:PSS 
 TA 是否含单宁酸 
 rGO 是否含还原氧化石墨烯 
 PPy 是否含聚吡咯 
 拉伸应变 目标变量：拉伸应变（%）

输入：
 训练集：PVA_hydrogel_train.csv
 验证集：PVA_hydrogel_val.csv
 测试集：PVA_hydrogel_test.csv

输出：
 代码及输出图片：多模型.ipynb
 模型文件：best_pva_hydrogel_model_梯度提升.pkl
 模型信息：model_info.json（含特征重要性、超参数配置）
 分析报告：pva_hydrogel_analysis_report.json（完整实验记录与可视化结果）

 结果：
 💡 基于模型的材料设计建议:
  1. 优先优化以下特征:
     • PVA_DH: 重要性 0.6065
     • CC: 重要性 0.0635
     • PVA_Conc: 重要性 0.0383

  2. 建议的参数范围:
     • PVA_MW: >120,000 Da (高分子量促进链缠结)
     • PVA_DH: 98-99% (高水解度增强氢键)
     • PVA_Conc: 6-12% (适中浓度平衡网络结构)
     • FC: 2-4 cycles (适度冻融循环增强结晶)
     • CC: 2-8% (适量导电填料避免团聚)

  3. 推荐组合:
     • 高MW PVA + 适量冻融循环 + CaCl₂交联
     • 适中浓度 + rGO填料 + 硼砂交联
