# Proposal
#proposal 

### Goal
- Standardize the configuration classes and improve the execution logic of the **DCAExecutor** and **PositionExecutor**.

### Useful links before getting started:
- **Position Executor:**
	- Docs: https://hummingbot.org/v2-strategies/executors/positionexecutor/
	- Code: https://github.com/hummingbot/hummingbot/tree/master/hummingbot/strategy_v2/executors/position_executor
- **DCA Executor:**
	- Docs: https://hummingbot.org/v2-strategies/executors/dcaexecutor/
	- Code: https://github.com/hummingbot/hummingbot/tree/master/hummingbot/strategy_v2/executors/dca_executor

### What is expected:
- Configuration: 
	- Accept percentages or raw prices for take profit, stop loss, and trailing stop inputs 
	- Accept base or quote order amounts
	- Review possible normalizations and improvements.
- Execution:
	- 