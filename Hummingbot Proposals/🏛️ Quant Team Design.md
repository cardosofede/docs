#quant

## Introduction

The objective of this document is to explain all the tasks that are needed in order to have a continuous bot operation. We can divide them in the following categories:
- **Maintenance**
    - Review periodically the logs of the active bots
    - Run test cases to reproduce errors in the production bots locally
    - Create tickets and work with dev to fix the bugs
- **Infrastructure**
    - Deployment of the infrastructure on the cloud
    - Monitor the usage of the servers
    - Evaluate rate limits and process limits to optimize the infrastructure (limit of exchanges/pairs and strategies to run)
- **Development + Research**
    - Design new trading strategies
    - Fix bugs reported by maintenance
- **Operations + Portfolio Management**
    - Create configuration files for production bots
    - Create configuration files for experiments bots
    - Keep track of balances, deposits and withdrawals for all the accounts
    - Deploy and monitor bots operation
    - Analyze bot performance to improve configs

## Services
- Dashboard:
	- Real-time information of the active bots.
	- Performance analysis of previous bots.
	- Backtesting and deploy new bots though backend-api.
	- Monitor accounts risk and portfolio evolution.
- Backend-API
	- Bot orchestration
	- Files management
	- Backtesting
	- Market data
- Hummingbot: a new hummingbot instance is spawned for each new strategy that wants to be deployed and the lifecycle is managed though the backend-api.


## Bot Lifecycle
1. Generate a strategy idea or pick one of the current strategies.
2. Design a configuration for your needs, that can be making profits from the strategy or meeting the KPIs of a contract.
3. Backtest your configuration and iterate with the parameters and save the best configurations.
4. Deploy the configurations in the same bot.
5. Monitor everyday the performance and errors and based on your analysis you can stop a controller or the full bot.
6. Analyze the errors found in the previous run and deploy a improved version of the bot.


## Recurring tasks
### Daily
- Review bots info
	- PNL
	- Trading volume
	- Error logs
- Review client KPIs
	- Volume traded per day
	- Spread over time
	- Uptime provided
- Based on analysis
	- Start / Stop bots
	- Notify client potential issues
	- Notify developers bugs
### Weekly
- Analysis of historical bot runs
- Create / Modify configurations or strategies

## Procedures
- [[Deployment]] [Deployment](Deployment.md)
