# frozen_string_literal: true

# This file is part of adsync.
#
# adsync is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# adsync is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU Lesser General Public License for more details.
#
# You should have received a copy of the GNU Lesser General Public License
# along with adsync.  If not, see <http://www.gnu.org/licenses/>.
#
# Copyright 2018 Jean-Remy Falleri <jr.falleri@gmail.com>

require 'rubocop/rake_task'
require 'bundler/gem_tasks'
require 'rake/clean'

CLEAN.include '*.gem', 'pkg'

desc 'Run RuboCop on the lib directory'
RuboCop::RakeTask.new(:rubocop) do |task|
  task.patterns = ['bin/adsync', 'lib/*.rb', 'Gemfile', 'adsync.gemspec', 'Rakefile']
  task.fail_on_error = true
end

task default: %i[rubocop build]
