require 'rake'
require 'rake/remote_task'

set :domain, '192.168.192.168'
set :ssh_flags, [
    '-l',
    'vagrant',
    '-i',
    ".vagrant/machines/default/virtualbox/private_key",
    "-o StrictHostKeyChecking=no",
    "-o UserKnownHostsFile=/dev/null",
    "-o LogLevel=error"
]

desc 'Run the specs'
remote_task :spec do
    run 'docker run -i -v /app:/usr/src/app app_app npm test'
end