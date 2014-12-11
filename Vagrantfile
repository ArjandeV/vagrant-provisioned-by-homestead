require 'json'
require 'yaml'

VAGRANTFILE_API_VERSION = "2"

homesteadYamlPath = File.expand_path("./Homestead.yaml")
aliasesPath = File.expand_path("./provision/aliases")

require_relative './provision/scripts/homestead.rb'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
	if File.exists? aliasesPath then
		config.vm.provision "file", source: aliasesPath, destination: "~/.bash_aliases"
	end

	Homestead.configure(config, YAML::load(File.read(homesteadYamlPath)))
end
