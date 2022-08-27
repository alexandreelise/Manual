Dashboard
==========

Learn how to add a dashboard to your component:

In the installation script of your component you add a mnu item into the backend menu.
This is done in the manifest file:

```PHPx title="Menu item Component "
    <administration>
	    <menu>COM_EXAMPLE</menu>
	
	[.. ]
	</administration>
```

A parameter '< dashboard >' expands the menu entry with link to a dashboard for your component.
- It will make a dashboard icon appear next to the administrator menu item for the component
- The dashboard icon will click through to display modules assigned to the cpanel-example administrator module position
- The title and icon defined in the XML file will be used as the header and icon at the top of the component's dashboard page.


```PHPx title="Dashboard Link "
<administration>
	<menu img="class:calendar">
		COM_EXAMPLE
		<params>
			<dashboard>my-example</dashboard>
		</params>
	</menu>
	
	[..]
</administration>
```

Joomla provides now a dashboard for your component: position: cpanel-my-example. 

<div class="alert bg-warning"> 
Note: use lowercase and only "-", never underscore for the dashboard name. 
</div>

my-example or example are correct, my_example, Com-MY_EXAMPLE are wrong

 # Quicktask Icon 

Add a quicktask icon to your submenu item, enabling your users to add a items with a single click.
Note that all & must be escaped to &amp; for the file to be valid XML and be parsed by the installer

```PHPx title="Dashboard link "
<submenu>
	<menu link="option=com_example">
		COM_EXAMPLE
		<params>
			<menu-quicktask-title>>COM_EXAMPLE_MENU_TITLE</menu-quicktask-title>
			<menu-quicktask>index.php?option=com_example&amp;view=event&amp;layout=edit</menu-quicktask>
		</params>
	</menu>
</submenu>```