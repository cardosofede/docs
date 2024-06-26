# Proposal
#proposal 

### Goal
 - Improve the documentation of the v2 strategies since they are becoming mainstream in Hummingbot and the current information provided does not get into much details on how the framework works under the hood.

### Useful links before getting started:
- **Official Docs:** https://hummingbot.org/strategies/
- **Github code:** https://github.com/hummingbot/hummingbot-site/tree/main/docs/v2-strategies

### What is expected:
- **Strategies V2 page:** there are some concepts mixed and can be simplified generating more emphasis on when to use each strategy type (or just present the ones available in v2 to avoid confusion)
- **Content organization:** the current situation starts with 2 walkthroughs, seems like will be better to start with the architecture to provide a general overview of how the framework works (include the flowcharts and the content that Patrick showed me before), and then the walkthrough. The structure can look like similar to this:
	- **Strategy V2**
		- **Architecture**
			- Market Data Provider
			- Executors
			- Controllers
			- Scripts
		- **Getting started**
			- Hummingbot Deploy
			- Running from source
		- **Guides**
			- Coding a controller (directional, mm, custom)
			- Backtesting a controller using notebooks
			- Adding your controller to Hummingbot Deploy and creating a configuration page in the dashboard
- **Blog post:** blog post that we can add to our [Academy](https://hummingbot.org/academy/) explaining a custom strategy defined by the developer (nice to have not required)