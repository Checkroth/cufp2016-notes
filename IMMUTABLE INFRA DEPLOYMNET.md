#Intro
- Data lake
- Cloud infrastructure
- Can't afford hardware cost of maintaining throughput bursts
	- Goes from 0 activitiy to massive activity

# Batch
- 90% of batch processing data transforming / machine learning
- Run continuously at different intervals
- Value throughput over latency

# Problems
- Configuration, datamangement, batch process improvement of costs
- Value latency over throughput
- Online processing
	- Online processes run continuously
	- Continuous deployment without downtime
	- 100s of repos	
	- No dedicated ops / support
- Leasing
	- People who work in production
	- "A person's claim to a resource for a period of time"
	- Should be isolated (can't interact / interfere)
	- Automatic termination
- Financial and commercial benefits for solving these problems
- Solutions done in FP / Haskell mostly
- Complex Systems
	- Infra deployment is complex system

# Configuration
- Define operation config
	- Type check
	- Serialize
	- Store
- Every server has daemon in haskell
	- Reads config
	- Manages lifecycle, monitoring, registration

# Solutions
- All solutions have individual servers / infrastructure
- Want unifies solution for batch and online leasing
#Three types
## Lifecycle management
- Each has its own 
- Referred to as an 'amp'
	- Have the knobs to control
	- High scalability
## Scheduling Services
- Managing constraints with cost and time
- Controlling config knobs
- Handling task allocation
- Task defines:
	- Capability
	- Execution
- Task submitted to scheduler, finds capability that meets task's requirements
	- When found, task is allocated to resource
	- If none, scheduler controls how capability is scaled to make it
	- Tasks delayed / allocated at high resource costs
## Operational Services
- Multiple services for different problems
### Batch Processing
- 'Hydra'
- Distributed cron
- Dependant tasks
- Hydra Task
	- Runs at some time
	- Executes some command
	- Requirements met -> hydra submits task to scheulder
	- Task becomes monitored
### Online Processing
- Continuous deployment system
- Deployment starts with commit
- Gets picked up, published to store
- Start server, puts commit on newly started server
	- Actually two servers
- If deployed successfuly, they are "healthy/active"

####The perfect program
`update . calculate =<< read`
- Define *goal*
	- Encode every step in lifecycle deployment process
	- Establish task with given configuration
	- Check for health
- Deployment result is `Monad`
#### Versioning
- "Fingerprint"
	- User nick
	- Softare type
	- Permissions
	- Can be customized to fit needs
	- For ex. daily deploy -> fingerprint contains date