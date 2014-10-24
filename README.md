# Rebar-friendly fork of Erlang AMQP client

This is a fork of the [official RabbitMQ/AMQP Erlang client](https://github.com/rabbitmq/rabbitmq-erlang-client). 

It's meant to be included in your rebar projects in your rebar.config file:

		{deps, [
			{amqp_client, ".*", {git, "git://github.com/jbrisbin/amqp_client.git", {tag, "rabbitmq-3.4.0"}}}
		]}.

The "master" branch of this port is a simple re-packaging of the rabbit_common AMQP client dependency.

The "community" branch, however, is a port of the RabbitMQ source code with additional strict compilation checking turned on and the source code edited to eliminate warnings. It should be 100% compatible with the unaltered source code. The community branch is simply a tweak to allow projects that depend on rabbit_common to not have to deal with the warnings issued by the compiler in the unaltered RabbitMQ code.

To use the "community" branch in your project, which includes stricter compilation settings, add "-community" 
to the version tag:

		{deps, [
			{amqp_client, ".*", {git, "git://github.com/jbrisbin/amqp_client.git", {tag, "rabbitmq-3.4.0-community"}}}
		]}.

### License 

This package, just like the the RabbitMQ server, is licensed under the MPL. For the MPL, please see LICENSE-MPL-RabbitMQ.
