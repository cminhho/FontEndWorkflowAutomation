# Font-end Workflow Automation

## NPM 
NPM is a NodeJs package manager, publishes and manages node programs written in JavaScript and runs under Node.js platform.
$npm init

```sh
 $npm init
 $npm info bower
 $npm install -g bower
 $npm install bower -save-dev
 $npm update
```

## YEOMAN
Yeoman helps you to kickstart new project, prescribing best practices and tools to help you stay productive
### YO
Yo scaffolds out a new application, writing your Grunt configuration and pulling in relevant Grunt tasks and Bower dependencies that you might need for your build.

```sh
 $npm install -g yo
 $npm install -g generator-angular
 $npm install -g generator-webapp
 $yo webapp
 $yo angular
```

### GRUNT
Grunt is a way to automate operations and to performing repetitive tasks. Once you have done the configuratio the less work you have to do when doing minification, compilation, deployment, unit testing, image optimisation and etc

```sh
 $npm install grunt --save-dev
 $npm install grunt-cli --save-dev
```

Gruntfile.json (Sample minify with Grunt)
```sh
grunt.initConfig({
  clean: {
    src: ['build/app.js', 'build/vendor.js']
  },
  
  copy: {
    files: [{
      src: 'build/app.js',
      dest: 'build/dist/app.js'
    }]
  }
  
  concat: {
    'build/app.js': ['build/vendors.js', 'build/app.js']
  }
  
  // ... other task configurations ...
  
});
 
grunt.registerTask('build', ['clean', 'bower', 'browserify', 'concat', 'copy']);
```
