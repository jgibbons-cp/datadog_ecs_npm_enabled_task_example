Sample Task for Network Monitoring Support for ECS on EC2
--

This is based on the documentation located on the Datadog ECS [documentation]
(https://docs.datadoghq.com/integrations/amazon_ecs/?tab=awscli) and the base 
task definition [here] (https://docs.datadoghq.com/integrations/amazon_ecs/?tab=awscli#create-an-ecs-task).

1) The apparmor security option needs to be added to the ECS environment by:

a) ssh to ecs host  
b) `sudo vi /etc/ecs/ecs.config`  
c) adding the following environment variable `ECS_APPARMOR_CAPABLE=true`  
d) restarting the ECS agent  
 
 sample_ecs_task.json is a sample task with the base requirements to configure the Datadog agent for [network performance
 monitoring] (https://docs.datadoghq.com/network_performance_monitoring/installation/?tab=docker).
 
 The items that need to be configured are <API_KEY>, and the <TASK_DEF_ARN>.
 
 Have fun!