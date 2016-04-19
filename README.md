# ada-dialogs
Dialgos API for Cordova Projects using Angular. The org.apache.cordova.dialogs plugin is required.

## Requiriments:
* org.apache.cordova.dialogs
* Angular Translate

## Installation

<pre>
bower install ada-dialogs
</pre>

## Configuration 

By injecting the "dialogsProvider", you can change the dialogs title:

<pre>
dialogsProvider.useDialogTitles(
{
		alert  : 'Atenção',
		error  : 'Erro',
		info   : 'Application',
		confirm: 'Confirmação' 
	};
);
</pre>

You also can use the keycodes to a translate file:

<pre>
dialogsProvider.useDialogTitles(
{
		alert  : 'WARNING_MSG_KEY',
		error  : 'ERROR_MSG_KEY',
		info   : 'APP_NAME_KEY',
		confirm: 'CONFIRMATION_KEY' 
	};
);
</pre>

## Utilization

By injecting the "dialogs" service in the controller:

<pre>
dialogs.alert('msg content').then(function(){
...
});
</pre>

<pre>
dialogs.error('msg content').then(function(){
...
});
</pre>

<pre>
dialogs.info('msg content').then(function(){
...
});
</pre>

<pre>
dialogs.confirm('msg content','OK','CANCEL').then(function(){
    console.log('OK callback');
},function(){
    console.log('CANCEL callback');
})
</pre>
