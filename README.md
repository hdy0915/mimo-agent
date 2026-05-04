# mimo-agent
本项目构建了一个双 Agent 协同工作流：  监控诊断 Agent （Analyzer）： 实时接入系统 Prometheus 指标与链路追踪数据。利用 MiMo 系列模型 的长文本处理能力，对异常时段的原始日志进行语义化扫描。  优化建议 Agent （Optimizer）： 当 Analyzer 确定瓶颈点后，Optimizer 会结合代码库历史提交记录，生成针对性的代码优化补丁（Refactor PR）或配置调整方案（如 JVM 参数、数据库索引优化）。  闭环验证： 包含长链推理能力，Agent 会在灰度环境自动运行 Benchmark 测试，对比优化前后的QPS和Laten cy数据，确保性能提升后再提交最终 Merge Request。
