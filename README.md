# Rebar-friendly fork of Erlang AMQP client

This is a fork of the [official RabbitMQ/AMQP Erlang client](https://github.com/rabbitmq/rabbitmq-erlang-client). 

It's meant to be included in your rebar projects in your rebar.config file:

		{deps, [
			{amqp_client, ".*", {git, "git://github.com/jbrisbin/amqp_client.git", {tag, "rabbitmq_2.6.0"}}}
		]}.

This is simply a re-packaging of the AMQP client, which is licensed under the MPL:

		This package, the RabbitMQ server is licensed under the MPL. For the
		MPL, please see LICENSE-MPL-RabbitMQ.

		If you have any questions regarding licensing, please contact us at
		info@rabbitmq.com.
