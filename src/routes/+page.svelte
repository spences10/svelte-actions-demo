<script lang="ts">
	import {
		DetailsAction,
		DetailsActionCustomEvent,
		DetailsTransition,
	} from '$lib/components'
</script>

<details class="border-4 rounded-lg border-primary mt-[30vh]">
	<summary class='p-4'>
		HTTP response status codes indicate whether a specific HTTP
		request has been successfully completed. Responses are grouped in
		five classes:
	</summary>
	<ol class="list-decimal px-12">
		<li>Informational responses (100 - 199)</li>
		<li>Successful responses (200 - 299)</li>
		<li>Redirection messages (300 - 399)</li>
		<li>Client error responses (400 - 499)</li>
		<li class="pb-5">Server error responses (500 - 599)</li>
	</ol>
</details>

<div class="mt-[70vh]" />

<DetailsTransition
	text="HTTP response status codes indicate whether a specific HTTP
  request has been successfully completed. Responses are grouped
  in five classes:"
>
	<ol class="list-decimal px-20">
		<li>Informational responses (100 - 199)</li>
		<li>Successful responses (200 - 299)</li>
		<li>Redirection messages (300 - 399)</li>
		<li>Client error responses (400 - 499)</li>
		<li class="pb-5">Server error responses (500 - 599)</li>
	</ol>
</DetailsTransition>

<div class="mt-[70vh]" />

<DetailsAction
	text="HTTP response status codes indicate whether a specific HTTP
  request has been successfully completed. Responses are grouped
  in five classes:"
>
	<ol class="list-decimal px-20">
		<li>Informational responses (100 - 199)</li>
		<li>Successful responses (200 - 299)</li>
		<li>Redirection messages (300 - 399)</li>
		<li>Client error responses (400 - 499)</li>
		<li class="pb-5">Server error responses (500 - 599)</li>
	</ol>
</DetailsAction>

<div class="mt-[70vh]" />

<DetailsActionCustomEvent
	text="HTTP response status codes indicate whether a specific HTTP
  request has been successfully completed. Responses are grouped
  in five classes:"
>
	<ol class="list-decimal px-20">
		<li>Informational responses (100 - 199)</li>
		<li>Successful responses (200 - 299)</li>
		<li>Redirection messages (300 - 399)</li>
		<li>Client error responses (400 - 499)</li>
		<li class="pb-5">Server error responses (500 - 599)</li>
	</ol>
</DetailsActionCustomEvent>

<div class='mt-[70vh]'></div>