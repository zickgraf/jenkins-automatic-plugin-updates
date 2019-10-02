println(Jenkins.instance.pluginManager.doCheckUpdatesServer());

plugins = Jenkins.instance.pluginManager.getPlugins();

for (plugin in plugins) {
	if (plugin.hasUpdate()) {
		println("Updating plugin '" + plugin.getDisplayName() + "'");
		println(plugin.getUpdateInfo().deploy(true).get());
	}
}

println(Jenkins.instance.doSafeRestart());
