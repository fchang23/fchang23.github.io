desc "build the project in dev"
task :build_dev do
  system("jekyll build")
end


desc "build the project in prod and copy to deployment folder"
task :build_prod do
  system("JEKYLL_ENV=production jekyll build")
  FileUtils.cp_r('_site/.', '../fchang23.github.io')
  FileUtils.chdir('../fchang23.github.io')
  system('git add .')
  system('git commit -m "update"')
  system('git push')
end
