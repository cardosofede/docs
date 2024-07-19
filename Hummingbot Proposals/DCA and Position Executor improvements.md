# Proposal
#proposal 

### Bounty amount $1500
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
	- Review and improve the control task logic
	- Define a better standard for the control shutdown process (currently is very messy)
	- Add functionality to use the connector to query the state of the order in case that the connector didn't managed the lifecycle of the order well
	- Evaluate if makes sense to accept early stop with "skip_shutdown" (this will not reverse the trade) or if it's better to have another executor that just has one open order an it's not closing it, like the TWAP executor that just places orders in one side.
	- Improve the close types, currently if we call the early stop method and the executor was not filled will appear as EARLY_STOP, if the order wasn't filled this is just canceling the open order and if the order was filled will be reversing it, but the two of them will have the same close type (usually the first scenario is for order refreshed and we can call it CANCELED or something like that)
	- General improvements that will benefit the efficiency of the executors are welcome.