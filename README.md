# api documentation for  [swagger-tools (v0.10.1)](https://github.com/apigee-127/swagger-tools)  [![npm package](https://img.shields.io/npm/v/npmdoc-swagger-tools.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-swagger-tools) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-swagger-tools.svg)](https://travis-ci.org/npmdoc/node-npmdoc-swagger-tools)
#### Various tools for using and integrating with Swagger.

[![NPM](https://nodei.co/npm/swagger-tools.png?downloads=true)](https://www.npmjs.com/package/swagger-tools)

[![apidoc](https://npmdoc.github.io/node-npmdoc-swagger-tools/build/screenCapture.buildNpmdoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-swagger-tools%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-swagger-tools/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-swagger-tools/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-swagger-tools/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jeremy Whitlock",
        "email": "jwhitlock@apache.org",
        "url": "https://github.com/whitlockjc"
    },
    "bin": {
        "swagger-tools": "./bin/swagger-tools"
    },
    "bugs": {
        "url": "https://github.com/apigee-127/swagger-tools/issues"
    },
    "dependencies": {
        "async": "^1.3.0",
        "body-parser": "1.12.4",
        "commander": "^2.8.1",
        "debug": "^2.2.0",
        "js-yaml": "^3.3.1",
        "json-refs": "^2.1.5",
        "lodash-compat": "^3.10.0",
        "multer": "^1.1.0",
        "parseurl": "^1.3.0",
        "path-to-regexp": "^1.2.0",
        "qs": "^4.0.0",
        "serve-static": "^1.10.0",
        "spark-md5": "^1.0.0",
        "string": "^3.3.0",
        "superagent": "^1.2.0",
        "swagger-converter": "^0.1.7",
        "traverse": "^0.6.6",
        "z-schema": "^3.15.4"
    },
    "description": "Various tools for using and integrating with Swagger.",
    "devDependencies": {
        "browserify": "^10.2.4",
        "connect": "^3.4.0",
        "del": "^1.2.0",
        "exposify": "^0.4.3",
        "gulp": "^3.9.0",
        "gulp-if": "^1.2.5",
        "gulp-istanbul": "^0.10.0",
        "gulp-jshint": "^1.11.2",
        "gulp-load-plugins": "^0.10.0",
        "gulp-mocha": "^2.1.3",
        "gulp-uglify": "^1.2.0",
        "jshint-stylish": "^2.0.1",
        "karma": "^0.13.3",
        "karma-mocha": "^0.2.0",
        "karma-mocha-reporter": "^1.0.4",
        "karma-phantomjs-launcher": "^0.2.0",
        "mocha": "^2.2.5",
        "phantomjs": "^1.9.17",
        "run-sequence": "^1.1.1",
        "supertest": "^1.0.1",
        "vinyl-browserify": "0.0.0",
        "vinyl-buffer": "^1.0.0",
        "vinyl-source-stream": "^1.1.0"
    },
    "directories": {},
    "dist": {
        "shasum": "a455b257998ecf20de5b4e99bdcf1a709ab0fedc",
        "tarball": "https://registry.npmjs.org/swagger-tools/-/swagger-tools-0.10.1.tgz"
    },
    "files": [
        "bin",
        "index.js",
        "LICENSE",
        "lib",
        "middleware",
        "schemas"
    ],
    "gitHead": "310d1dedbb88a3de328fc421b261e0566ffbf2af",
    "homepage": "https://github.com/apigee-127/swagger-tools",
    "keywords": [
        "api",
        "connect",
        "middleware",
        "swagger"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "whitlockjc",
            "email": "jwhitlock@apache.org"
        }
    ],
    "name": "swagger-tools",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/apigee-127/swagger-tools.git"
    },
    "scripts": {
        "test": "./node_modules/gulp/bin/gulp.js"
    },
    "version": "0.10.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module swagger-tools](#apidoc.module.swagger-tools)
1.  [function <span class="apidocSignatureSpan">swagger-tools.</span>initializeMiddleware (rlOrSO, resources, callback)](#apidoc.element.swagger-tools.initializeMiddleware)
1.  object <span class="apidocSignatureSpan">swagger-tools.</span>helpers
1.  object <span class="apidocSignatureSpan">swagger-tools.</span>specs
1.  object <span class="apidocSignatureSpan">swagger-tools.</span>validators

#### [module swagger-tools.helpers](#apidoc.module.swagger-tools.helpers)
1.  [function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>createJsonValidator (schemas)](#apidoc.element.swagger-tools.helpers.createJsonValidator)
1.  [function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>formatResults (results)](#apidoc.element.swagger-tools.helpers.formatResults)
1.  [function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>getErrorCount (results)](#apidoc.element.swagger-tools.helpers.getErrorCount)
1.  [function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>getSpec (version, throwError)](#apidoc.element.swagger-tools.helpers.getSpec)
1.  [function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>getSwaggerVersion (document)](#apidoc.element.swagger-tools.helpers.getSwaggerVersion)
1.  [function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>printValidationResults (version, apiDOrSO, apiDeclarations, results, printSummary)](#apidoc.element.swagger-tools.helpers.printValidationResults)
1.  [function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>registerCustomFormats (json)](#apidoc.element.swagger-tools.helpers.registerCustomFormats)
1.  object <span class="apidocSignatureSpan">swagger-tools.helpers.</span>swaggerOperationMethods

#### [module swagger-tools.validators](#apidoc.module.swagger-tools.validators)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateAgainstSchema (schemaOrName, data, validator)](#apidoc.element.swagger-tools.validators.validateAgainstSchema)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateArrayType (schema)](#apidoc.element.swagger-tools.validators.validateArrayType)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateContentType (gPOrC, oPOrC, reqOrRes)](#apidoc.element.swagger-tools.validators.validateContentType)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateEnum (val, allowed)](#apidoc.element.swagger-tools.validators.validateEnum)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMaxItems (val, maxItems)](#apidoc.element.swagger-tools.validators.validateMaxItems)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMaxLength (val, maxLength)](#apidoc.element.swagger-tools.validators.validateMaxLength)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMaxProperties (val, maxProperties)](#apidoc.element.swagger-tools.validators.validateMaxProperties)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMaximum (val, maximum, type, exclusive)](#apidoc.element.swagger-tools.validators.validateMaximum)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMinItems (val, minItems)](#apidoc.element.swagger-tools.validators.validateMinItems)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMinLength (val, minLength)](#apidoc.element.swagger-tools.validators.validateMinLength)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMinProperties (val, minProperties)](#apidoc.element.swagger-tools.validators.validateMinProperties)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMinimum (val, minimum, type, exclusive)](#apidoc.element.swagger-tools.validators.validateMinimum)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMultipleOf (val, multipleOf)](#apidoc.element.swagger-tools.validators.validateMultipleOf)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validatePattern (val, pattern)](#apidoc.element.swagger-tools.validators.validatePattern)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateRequiredness (val, required)](#apidoc.element.swagger-tools.validators.validateRequiredness)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateSchemaConstraints (version, schema, path, val)](#apidoc.element.swagger-tools.validators.validateSchemaConstraints)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateTypeAndFormat (version, val, type, format, allowEmptyValue, skipError)](#apidoc.element.swagger-tools.validators.validateTypeAndFormat)
1.  [function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateUniqueItems (val, isUnique)](#apidoc.element.swagger-tools.validators.validateUniqueItems)



# <a name="apidoc.module.swagger-tools"></a>[module swagger-tools](#apidoc.module.swagger-tools)

#### <a name="apidoc.element.swagger-tools.initializeMiddleware"></a>[function <span class="apidocSignatureSpan">swagger-tools.</span>initializeMiddleware (rlOrSO, resources, callback)](#apidoc.element.swagger-tools.initializeMiddleware)
- description and source-code
```javascript
function initializeMiddleware(rlOrSO, resources, callback) {
  var args;
  var spec;

  debug('Initializing middleware');

  if (_.isUndefined(rlOrSO)) {
    throw new Error('rlOrSO is required');
  } else if (!_.isPlainObject(rlOrSO)) {
    throw new TypeError('rlOrSO must be an object');
  }

  args = [rlOrSO];
  spec = helpers.getSpec(helpers.getSwaggerVersion(rlOrSO), true);

  debug('  Identified Swagger version: %s', spec.version);

  if (spec.version === '1.2') {
    if (_.isUndefined(resources)) {
      throw new Error('resources is required');
    } else if (!_.isArray(resources)) {
      throw new TypeError('resources must be an array');
    }

    debug('  Number of API Declarations: %d', resources.length);

    args.push(resources);
  } else {
    callback = arguments[1];
  }

  if (_.isUndefined(callback)) {
    throw new Error('callback is required');
  } else if (!_.isFunction(callback)) {
    throw new TypeError('callback must be a function');
  }

  args.push(function (err, results) {
    if (results && results.errors.length + _.reduce(results.apiDeclarations || [], function (count, apiDeclaration) {
      return count += (apiDeclaration ? apiDeclaration.errors.length : 0);
    }, 0) > 0) {
      err = new Error('Swagger document(s) failed validation so the server cannot start');

      err.failedValidation = true;
      err.results = results;
    }

    debug('  Validation: %s', err ? 'failed' : 'succeeded');

    try {
      if (err) {
        throw err;
      }

      callback({
        // Create a wrapper to avoid having to pass the non-optional arguments back to the swaggerMetadata middleware
        swaggerMetadata: function () {
          var swaggerMetadata = require('./middleware/swagger-metadata');

          return swaggerMetadata.apply(undefined, args.slice(0, args.length - 1));
        },
        swaggerRouter: require('./middleware/swagger-router'),
        swaggerSecurity: require('./middleware/swagger-security'),
        // Create a wrapper to avoid having to pass the non-optional arguments back to the swaggerUi middleware
        swaggerUi: function (options) {
          var swaggerUi = require('./middleware/swagger-ui');
          var suArgs = [rlOrSO];

          if (spec.version === '1.2') {
            suArgs.push(_.reduce(resources, function (map, resource) {
              map[resource.resourcePath] = resource;

              return map;
            }, {}));
          }

          suArgs.push(options || {});

          return swaggerUi.apply(undefined, suArgs);
        },
        swaggerValidator: require('./middleware/swagger-validator')
      });
    } catch (err) {
      if (process.env.RUNNING_SWAGGER_TOOLS_TESTS === 'true') {
        // When running the swagger-tools test suite, we want to return an error instead of exiting the process.  This
        // does not mean that this function is an error-first callback but due to json-refs using Promises, we have to
        // return the error to avoid the error being swallowed.
        callback(err);
      } else {
        if (err.failedValidation === true) {
          helpers.printValidationResults(spec.version, rlOrSO, resources, results, true);
        } else {
          console.error('Error initializing middleware');
          console.error(err.stack);
        }

        process.exit(1);
      }
    }
  });

  spec.validate.apply(spec, args);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.swagger-tools.helpers"></a>[module swagger-tools.helpers](#apidoc.module.swagger-tools.helpers)

#### <a name="apidoc.element.swagger-tools.helpers.createJsonValidator"></a>[function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>createJsonValidator (schemas)](#apidoc.element.swagger-tools.helpers.createJsonValidator)
- description and source-code
```javascript
createJsonValidator = function (schemas) {
  var validator = new ZSchema({
    breakOnFirstError: false,
    reportPathAsArray: true
  });
  var result;

  // Add the draft-04 spec
  validator.setRemoteReference(draft04Url, draft04Json);

  // Swagger uses some unsupported/invalid formats so just make them all pass
  _.each(customJsonSchemaFormats, function (format) {
    ZSchema.registerFormat(format, function () {
      return true;
    });
  });

  // Compile and validate the schemas
  if (!_.isUndefined(schemas)) {
    result = validator.compileSchema(schemas);

    // If there is an error, it's unrecoverable so just blow the eff up
    if (result === false) {
      console.error('JSON Schema file' + (schemas.length > 1 ? 's are' : ' is') + ' invalid:');

      _.each(validator.getLastErrors(), function (err) {
        console.error('  ' + (_.isArray(err.path) ? JsonRefs.pathToPtr(err.path) : err.path) + ': ' + err.message);
      });

      throw new Error('Unable to create validator due to invalid JSON Schema');
    }
  }

  return validator;
}
```
- example usage
```shell
...
    .catch(callback);
} else {
  callback();
}
};

var validateAgainstSchema = function (spec, schemaOrName, data, callback) {
var validator = _.isString(schemaOrName) ? spec.validators[schemaOrName] : helpers.createJsonValidator();

helpers.registerCustomFormats(data);

try {
  validators.validateAgainstSchema(schemaOrName, data, validator);
} catch (err) {
  if (err.failedValidation) {
...
```

#### <a name="apidoc.element.swagger-tools.helpers.formatResults"></a>[function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>formatResults (results)](#apidoc.element.swagger-tools.helpers.formatResults)
- description and source-code
```javascript
formatResults = function (results) {
  if (results) {
    // Update the results based on its content to indicate success/failure accordingly
    results = (results.errors.length + results.warnings.length +
    _.reduce(results.apiDeclarations, function (count, aResult) {
      if (aResult) {
        count += aResult.errors.length + aResult.warnings.length;
      }

      return count;
    }, 0) > 0) ? results : undefined;
  }

  return results;
}
```
- example usage
```shell
...
  validateDefinitions(documentMetadata, results);

  callback(undefined, results);
};

var validateSemantically = function (spec, rlOrSO, apiDeclarations, callback) {
  var cbWrapper = function (err, results) {
    callback(err, helpers.formatResults(results));
  };
  if (spec.version === '1.2') {
    validateSwagger1_2(spec, rlOrSO, apiDeclarations, cbWrapper); // jshint ignore:line
  } else {
    validateSwagger2_0(spec, rlOrSO, cbWrapper); // jshint ignore:line
  }
};
...
```

#### <a name="apidoc.element.swagger-tools.helpers.getErrorCount"></a>[function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>getErrorCount (results)](#apidoc.element.swagger-tools.helpers.getErrorCount)
- description and source-code
```javascript
getErrorCount = function (results) {
  var errors = 0;

  if (results) {
    errors = results.errors.length;

    _.each(results.apiDeclarations, function (adResults) {
      if (adResults) {
        errors += adResults.errors.length;
      }
    });
  }

  return errors;
}
```
- example usage
```shell
...
Specification.prototype.composeModel = function (apiDOrSO, modelIdOrRef, callback) {
  var swaggerVersion = helpers.getSwaggerVersion(apiDOrSO);
  var doComposition = function (err, results) {
var documentMetadata;

if (err) {
  return callback(err);
} else if (helpers.getErrorCount(results) > 0) {
  return handleValidationError(results, callback);
}

documentMetadata = getDocumentCache(apiDOrSO);
results = {
  errors: [],
  warnings: []
...
```

#### <a name="apidoc.element.swagger-tools.helpers.getSpec"></a>[function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>getSpec (version, throwError)](#apidoc.element.swagger-tools.helpers.getSpec)
- description and source-code
```javascript
getSpec = function (version, throwError) {
  var spec;

  version = coerceVersion(version);
  spec = specCache[version];

  if (_.isUndefined(spec)) {
    switch (version) {
    case '1.2':
      spec = require('../lib/specs').v1_2; // jshint ignore:line

      break;

    case '2.0':
      spec = require('../lib/specs').v2_0; // jshint ignore:line

      break;

    default:
      if (throwError === true) {
        throw new Error('Unsupported Swagger version: ' + version);
      }
    }
  }

  return spec;
}
```
- example usage
```shell
...
if (_.isUndefined(rlOrSO)) {
  throw new Error('rlOrSO is required');
} else if (!_.isPlainObject(rlOrSO)) {
  throw new TypeError('rlOrSO must be an object');
}

args = [rlOrSO];
spec = helpers.getSpec(helpers.getSwaggerVersion(rlOrSO), true);

debug('  Identified Swagger version: %s', spec.version);

if (spec.version === '1.2') {
  if (_.isUndefined(resources)) {
    throw new Error('resources is required');
  } else if (!_.isArray(resources)) {
...
```

#### <a name="apidoc.element.swagger-tools.helpers.getSwaggerVersion"></a>[function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>getSwaggerVersion (document)](#apidoc.element.swagger-tools.helpers.getSwaggerVersion)
- description and source-code
```javascript
getSwaggerVersion = function (document) {
  return _.isPlainObject(document) ? coerceVersion(document.swaggerVersion || document.swagger) : undefined;
}
```
- example usage
```shell
...
if (_.isUndefined(rlOrSO)) {
  throw new Error('rlOrSO is required');
} else if (!_.isPlainObject(rlOrSO)) {
  throw new TypeError('rlOrSO must be an object');
}

args = [rlOrSO];
spec = helpers.getSpec(helpers.getSwaggerVersion(rlOrSO), true);

debug('  Identified Swagger version: %s', spec.version);

if (spec.version === '1.2') {
  if (_.isUndefined(resources)) {
    throw new Error('resources is required');
  } else if (!_.isArray(resources)) {
...
```

#### <a name="apidoc.element.swagger-tools.helpers.printValidationResults"></a>[function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>printValidationResults (version, apiDOrSO, apiDeclarations, results, printSummary)](#apidoc.element.swagger-tools.helpers.printValidationResults)
- description and source-code
```javascript
printValidationResults = function (version, apiDOrSO, apiDeclarations, results, printSummary) {
  var hasErrors = getErrorCount(results) > 0;
  var stream = hasErrors ? console.error : console.log;
  var pluralize = function (string, count) {
    return count === 1 ? string : string + 's';
  };
  var printErrorsOrWarnings = function (header, entries, indent) {
    if (header) {
      stream(header + ':');
      stream();
    }

    _.each(entries, function (entry) {
      stream(new Array(indent + 1).join(' ') + JsonRefs.pathToPtr(entry.path) + ': ' + entry.message);

      if (entry.inner) {
        printErrorsOrWarnings (undefined, entry.inner, indent + 2);
      }
    });

    if (header) {
      stream();
    }
  };
  var errorCount = 0;
  var warningCount = 0;

  stream();

  if (results.errors.length > 0) {
    errorCount += results.errors.length;

    printErrorsOrWarnings('API Errors', results.errors, 2);
  }

  if (results.warnings.length > 0) {
    warningCount += results.warnings.length;

    printErrorsOrWarnings('API Warnings', results.warnings, 2);
  }

  if (results.apiDeclarations) {
    results.apiDeclarations.forEach(function (adResult, index) {
      if (!adResult) {
        return;
      }

      var name = apiDeclarations[index].resourcePath || index;

      if (adResult.errors.length > 0) {
        errorCount += adResult.errors.length;

        printErrorsOrWarnings('  API Declaration (' + name + ') Errors', adResult.errors, 4);
      }

      if (adResult.warnings.length > 0) {
        warningCount += adResult.warnings.length;

        printErrorsOrWarnings('  API Declaration (' + name + ') Warnings', adResult.warnings, 4);
      }
    });
  }

  if (printSummary) {
    if (errorCount > 0) {
      stream(errorCount + ' ' + pluralize('error', errorCount) + ' and ' + warningCount + ' ' +
                    pluralize('warning', warningCount));
    } else {
      stream('Validation succeeded but with ' + warningCount + ' ' + pluralize('warning', warningCount));
    }
  }

  stream();
}
```
- example usage
```shell
...
if (process.env.RUNNING_SWAGGER_TOOLS_TESTS === 'true') {
  // When running the swagger-tools test suite, we want to return an error instead of exiting the process.  This
  // does not mean that this function is an error-first callback but due to json-refs using Promises, we have to
  // return the error to avoid the error being swallowed.
  callback(err);
} else {
  if (err.failedValidation === true) {
    helpers.printValidationResults(spec.version, rlOrSO, resources, results, true);
  } else {
    console.error('Error initializing middleware');
    console.error(err.stack);
  }

  process.exit(1);
}
...
```

#### <a name="apidoc.element.swagger-tools.helpers.registerCustomFormats"></a>[function <span class="apidocSignatureSpan">swagger-tools.helpers.</span>registerCustomFormats (json)](#apidoc.element.swagger-tools.helpers.registerCustomFormats)
- description and source-code
```javascript
registerCustomFormats = function (json) {
  traverse(json).forEach(function () {
    var name = this.key;
    var format = this.node;

    if (name === 'format' && _.indexOf(ZSchema.getRegisteredFormats(), format) === -1) {
      ZSchema.registerFormat(format, function () {
        return true;
      });
    }
  });
}
```
- example usage
```shell
...
  callback();
}
};

var validateAgainstSchema = function (spec, schemaOrName, data, callback) {
var validator = _.isString(schemaOrName) ? spec.validators[schemaOrName] : helpers.createJsonValidator();

helpers.registerCustomFormats(data);

try {
  validators.validateAgainstSchema(schemaOrName, data, validator);
} catch (err) {
  if (err.failedValidation) {
    return callback(undefined, err.results);
  } else {
...
```



# <a name="apidoc.module.swagger-tools.validators"></a>[module swagger-tools.validators](#apidoc.module.swagger-tools.validators)

#### <a name="apidoc.element.swagger-tools.validators.validateAgainstSchema"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateAgainstSchema (schemaOrName, data, validator)](#apidoc.element.swagger-tools.validators.validateAgainstSchema)
- description and source-code
```javascript
validateAgainstSchema = function (schemaOrName, data, validator) {
  var sanitizeError = function (obj) {
    // Make anyOf/oneOf errors more human readable (Issue 200)
    var defType = ['additionalProperties', 'items'].indexOf(obj.path[obj.path.length - 1]) > -1 ?
          'schema' :
          obj.path[obj.path.length - 2];

    if (['ANY_OF_MISSING', 'ONE_OF_MISSING'].indexOf(obj.code) > -1) {
      switch (defType) {
      case 'parameters':
        defType = 'parameter';
        break;

      case 'responses':
        defType = 'response';
        break;

      case 'schema':
        defType += ' ' + obj.path[obj.path.length - 1];

        // no default
      }

      obj.message = 'Not a valid ' + defType + ' definition';
    }

    // Remove the params portion of the error
    delete obj.params;
    delete obj.schemaId;

    if (obj.inner) {
      _.each(obj.inner, function (nObj) {
        sanitizeError(nObj);
      });
    }
  };
  var schema = _.isPlainObject(schemaOrName) ? _.cloneDeep(schemaOrName) : schemaOrName;

  // We don't check this due to internal usage but if validator is not provided, schemaOrName must be a schema
  if (_.isUndefined(validator)) {
    validator = helpers.createJsonValidator([schema]);
  }

  var valid = validator.validate(data, schema);

  if (!valid) {
    try {
      throwErrorWithCode('SCHEMA_VALIDATION_FAILED', 'Failed schema validation');
    } catch (err) {
      err.results = {
        errors: _.map(validator.getLastErrors(), function (err) {
          sanitizeError(err);

          return err;
        }),
        warnings: []
      };

      throw err;
    }
  }
}
```
- example usage
```shell
...

var validateAgainstSchema = function (spec, schemaOrName, data, callback) {
var validator = _.isString(schemaOrName) ? spec.validators[schemaOrName] : helpers.createJsonValidator();

helpers.registerCustomFormats(data);

try {
  validators.validateAgainstSchema(schemaOrName, data, validator);
} catch (err) {
  if (err.failedValidation) {
    return callback(undefined, err.results);
  } else {
    return callback(err);
  }
}
...
```

#### <a name="apidoc.element.swagger-tools.validators.validateArrayType"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateArrayType (schema)](#apidoc.element.swagger-tools.validators.validateArrayType)
- description and source-code
```javascript
validateArrayType = function (schema) {
  // We have to do this manually for now
  if (schema.type === 'array' && _.isUndefined(schema.items)) {
    throwErrorWithCode('OBJECT_MISSING_REQUIRED_PROPERTY', 'Missing required property: items');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateContentType"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateContentType (gPOrC, oPOrC, reqOrRes)](#apidoc.element.swagger-tools.validators.validateContentType)
- description and source-code
```javascript
validateContentType = function (gPOrC, oPOrC, reqOrRes) {
  // http://www.w3.org/Protocols/rfc2616/rfc2616-sec7.html#sec7.2.1
  var isResponse = typeof reqOrRes.end === 'function';
  var contentType = isResponse ? reqOrRes.getHeader('content-type') : reqOrRes.headers['content-type'];
  var pOrC = _.map(_.union(gPOrC, oPOrC), function (contentType) {
    return contentType.split(';')[0];
  });

  if (!contentType) {
    if (isResponse) {
      contentType = 'text/plain';
    } else {
      contentType = 'application/octet-stream';
    }
  }

  contentType = contentType.split(';')[0];

  if (pOrC.length > 0 && (isResponse ?
                          true :
                          ['POST', 'PUT'].indexOf(reqOrRes.method) !== -1) && pOrC.indexOf(contentType) === -1) {
    throw new Error('Invalid content type (' + contentType + ').  These are valid: ' + pOrC.join(', '));
  }
}
```
- example usage
```shell
...
      sendData(swaggerVersion, res, data, encoding, true);
      return; // do NOT call next() here, doing so would execute remaining middleware chain twice
    }

    try {
      // Validate the content type
      try {
validators.validateContentType(req.swagger.apiDeclaration ?
                                 req.swagger.apiDeclaration.produces :
                                 req.swagger.swaggerObject.produces,
                               operation.produces, res);
      } catch (err) {
err.failedValidation = true;

throw err;
...
```

#### <a name="apidoc.element.swagger-tools.validators.validateEnum"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateEnum (val, allowed)](#apidoc.element.swagger-tools.validators.validateEnum)
- description and source-code
```javascript
validateEnum = function (val, allowed) {
  if (!_.isUndefined(allowed) && !_.isUndefined(val) && allowed.indexOf(val) === -1) {
    throwErrorWithCode('ENUM_MISMATCH', 'Not an allowable value (' + allowed.join(', ') + '): ' + val);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateMaxItems"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMaxItems (val, maxItems)](#apidoc.element.swagger-tools.validators.validateMaxItems)
- description and source-code
```javascript
validateMaxItems = function (val, maxItems) {
  if (!_.isUndefined(maxItems) && val.length > maxItems) {
    throwErrorWithCode('ARRAY_LENGTH_LONG', 'Array is too long (' + val.length + '), maximum ' + maxItems);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateMaxLength"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMaxLength (val, maxLength)](#apidoc.element.swagger-tools.validators.validateMaxLength)
- description and source-code
```javascript
validateMaxLength = function (val, maxLength) {
  if (!_.isUndefined(maxLength) && val.length > maxLength) {
    throwErrorWithCode('MAX_LENGTH', 'String is too long (' + val.length + ' chars), maximum ' + maxLength);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateMaxProperties"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMaxProperties (val, maxProperties)](#apidoc.element.swagger-tools.validators.validateMaxProperties)
- description and source-code
```javascript
validateMaxProperties = function (val, maxProperties) {
  var propCount = _.isPlainObject(val) ? Object.keys(val).length : 0;

  if (!_.isUndefined(maxProperties) && propCount > maxProperties) {
    throwErrorWithCode('MAX_PROPERTIES',
                       'Number of properties is too many (' + propCount + ' properties), maximum ' + maxProperties);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateMaximum"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMaximum (val, maximum, type, exclusive)](#apidoc.element.swagger-tools.validators.validateMaximum)
- description and source-code
```javascript
validateMaximum = function (val, maximum, type, exclusive) {
  var code = exclusive === true ? 'MAXIMUM_EXCLUSIVE' : 'MAXIMUM';
  var testMax;
  var testVal;

  if (_.isUndefined(exclusive)) {
    exclusive = false;
  }

  if (type === 'integer') {
    testVal = parseInt(val, 10);
  } else if (type === 'number') {
    testVal = parseFloat(val);
  }

  if (!_.isUndefined(maximum)) {
    testMax = parseFloat(maximum);

    if (exclusive && testVal >= testMax) {
      throwErrorWithCode(code, 'Greater than or equal to the configured maximum (' + maximum + '): ' + val);
    } else if (testVal > testMax) {
      throwErrorWithCode(code, 'Greater than the configured maximum (' + maximum + '): ' + val);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateMinItems"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMinItems (val, minItems)](#apidoc.element.swagger-tools.validators.validateMinItems)
- description and source-code
```javascript
validateMinItems = function (val, minItems) {
  if (!_.isUndefined(minItems) && val.length < minItems) {
    throwErrorWithCode('ARRAY_LENGTH_SHORT', 'Array is too short (' + val.length + '), minimum ' + minItems);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateMinLength"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMinLength (val, minLength)](#apidoc.element.swagger-tools.validators.validateMinLength)
- description and source-code
```javascript
validateMinLength = function (val, minLength) {
  if (!_.isUndefined(minLength) && val.length < minLength) {
    throwErrorWithCode('MIN_LENGTH', 'String is too short (' + val.length + ' chars), minimum ' + minLength);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateMinProperties"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMinProperties (val, minProperties)](#apidoc.element.swagger-tools.validators.validateMinProperties)
- description and source-code
```javascript
validateMinProperties = function (val, minProperties) {
  var propCount = _.isPlainObject(val) ? Object.keys(val).length : 0;

  if (!_.isUndefined(minProperties) && propCount < minProperties) {
    throwErrorWithCode('MIN_PROPERTIES',
                       'Number of properties is too few (' + propCount + ' properties), minimum ' + minProperties);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateMinimum"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMinimum (val, minimum, type, exclusive)](#apidoc.element.swagger-tools.validators.validateMinimum)
- description and source-code
```javascript
validateMinimum = function (val, minimum, type, exclusive) {
  var code = exclusive === true ? 'MINIMUM_EXCLUSIVE' : 'MINIMUM';
  var testMin;
  var testVal;

  if (_.isUndefined(exclusive)) {
    exclusive = false;
  }

  if (type === 'integer') {
    testVal = parseInt(val, 10);
  } else if (type === 'number') {
    testVal = parseFloat(val);
  }

  if (!_.isUndefined(minimum)) {
    testMin = parseFloat(minimum);

    if (exclusive && testVal <= testMin) {
      throwErrorWithCode(code, 'Less than or equal to the configured minimum (' + minimum + '): ' + val);
    } else if (testVal < testMin) {
      throwErrorWithCode(code, 'Less than the configured minimum (' + minimum + '): ' + val);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateMultipleOf"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateMultipleOf (val, multipleOf)](#apidoc.element.swagger-tools.validators.validateMultipleOf)
- description and source-code
```javascript
validateMultipleOf = function (val, multipleOf) {
  if (!_.isUndefined(multipleOf) && val % multipleOf !== 0) {
    throwErrorWithCode('MULTIPLE_OF', 'Not a multiple of ' + multipleOf);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validatePattern"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validatePattern (val, pattern)](#apidoc.element.swagger-tools.validators.validatePattern)
- description and source-code
```javascript
validatePattern = function (val, pattern) {
  if (!_.isUndefined(pattern) && _.isNull(val.match(new RegExp(pattern)))) {
    throwErrorWithCode('PATTERN', 'Does not match required pattern: ' + pattern);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateRequiredness"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateRequiredness (val, required)](#apidoc.element.swagger-tools.validators.validateRequiredness)
- description and source-code
```javascript
validateRequiredness = function (val, required) {
  if (!_.isUndefined(required) && required === true && _.isUndefined(val)) {
    throwErrorWithCode('REQUIRED', 'Is required');
  }
}
```
- example usage
```shell
...
paramName = schema.name;
paramPath = swaggerVersion === '1.2' ?
  req.swagger.operationPath.concat(['params', paramIndex.toString()]) :
  parameter.path;
val = req.swagger.params[paramName].value;

// Validate requiredness
validators.validateRequiredness(val, schema.required);

// Quick return if the value is not present
if (_.isUndefined(val)) {
  return oCallback();
}

validateValue(req, schema, paramPath, val, oCallback);
...
```

#### <a name="apidoc.element.swagger-tools.validators.validateSchemaConstraints"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateSchemaConstraints (version, schema, path, val)](#apidoc.element.swagger-tools.validators.validateSchemaConstraints)
- description and source-code
```javascript
validateSchemaConstraints = function (version, schema, path, val) {
  var resolveSchema = function (schema) {
    var resolved = schema;

    if (resolved.schema) {
      path = path.concat(['schema']);

      resolved = resolveSchema(resolved.schema);
    }

    return resolved;
  };

  var type = schema.type;
  var allowEmptyValue;

  if (!type) {
    if (!schema.schema) {
      if (path[path.length - 2] === 'responses') {
        type = 'void';
      } else {
        type = 'object';
      }
    } else {
      schema = resolveSchema(schema);
      type = schema.type || 'object';
    }
  }

  allowEmptyValue = schema ? schema.allowEmptyValue === true : false;

  try {
    // Always perform this check even if there is no value
    if (type === 'array') {
      validateArrayType(schema);
    }

    // Default to default value if necessary
    if (_.isUndefined(val)) {
      val = version === '1.2' ? schema.defaultValue : schema.default;

      path = path.concat([version === '1.2' ? 'defaultValue' : 'default']);
    }

    // If there is no explicit default value, return as all validations will fail
    if (_.isUndefined(val)) {
      return;
    }

    if (type === 'array') {
      _.each(val, function (val, index) {
        try {
          validateSchemaConstraints(version, schema.items || {}, path.concat(index.toString()), val);
        } catch (err) {
          err.message = 'Value at index ' + index + ' ' + (err.code === 'INVALID_TYPE' ? 'is ' : '') +
            err.message.charAt(0).toLowerCase() + err.message.substring(1);

          throw err;
        }
      });
    } else {
      validateTypeAndFormat(version, val, type, schema.format, allowEmptyValue);
    }

    // Validate enum
    validateEnum(val, schema.enum);

    // Validate maximum
    validateMaximum(val, schema.maximum, type, schema.exclusiveMaximum);


    // Validate maxItems (Swagger 2.0+)
    validateMaxItems(val, schema.maxItems);

    // Validate maxLength (Swagger 2.0+)
    validateMaxLength(val, schema.maxLength);

    // Validate maxProperties (Swagger 2.0+)
    validateMaxProperties(val, schema.maxProperties);

    // Validate minimum
    validateMinimum(val, schema.minimum, type, schema.exclusiveMinimum);

    // Validate minItems
    validateMinItems(val, schema.minItems);

    // Validate minLength (Swagger 2.0+)
    validateMinLength(val, schema.minLength);

    // Validate minProperties (Swagger 2.0+)
    validateMinProperties(val, schema.minProperties);

    // Validate multipleOf (Swagger 2.0+)
    validateMultipleOf(val, schema.multipleOf);

    // Validate pattern (Swagger 2.0+)
    validatePattern(val, schema.pattern);

    // Validate uniqueItems
    validateUniqueItems(val, schema.uniqueItems);
  } catch (err) {
    err.path = path;

    throw err;
  }
}
```
- example usage
```shell
...
  if (!_.isUndefined(data) && data.indexOf(val) > -1) {
    createErrorOrWarning('DUPLICATE_' + codeSuffix, msgPrefix + ' already defined: ' + val, path, dest);
  }
};

var validateSchemaConstraints = function (documentMetadata, schema, path, results, skip) {
  try {
    validators.validateSchemaConstraints(documentMetadata.swaggerVersion, schema, path, undefined);
  } catch (err) {
    if (!skip) {
      createErrorOrWarning(err.code, err.message, err.path, results.errors);
    }
  }
};
...
```

#### <a name="apidoc.element.swagger-tools.validators.validateTypeAndFormat"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateTypeAndFormat (version, val, type, format, allowEmptyValue, skipError)](#apidoc.element.swagger-tools.validators.validateTypeAndFormat)
- description and source-code
```javascript
function validateTypeAndFormat(version, val, type, format, allowEmptyValue, skipError) {
  var result = true;
  var oVal = val;

  // If there is an empty value and we allow empty values, the value is always valid
  if (allowEmptyValue === true && val === '') {
    return;
  }

  if (_.isArray(val)) {
    _.each(val, function (aVal, index) {
      if (!validateTypeAndFormat(version, aVal, type, format, allowEmptyValue, true)) {
        throwErrorWithCode('INVALID_TYPE', 'Value at index ' + index + ' is not a valid ' + type + ': ' + aVal);
      }
    });
  } else {
    switch (type) {
    case 'boolean':
      // Coerce the value only for Swagger 1.2
      if (version === '1.2' && _.isString(val)) {
        if (val === 'false') {
          val = false;
        } else if (val === 'true') {
          val = true;
        }
      }

      result = _.isBoolean(val);
      break;
    case 'integer':
      // Coerce the value only for Swagger 1.2
      if (version === '1.2' && _.isString(val)) {
        val = Number(val);
      }

      result = _.isFinite(val) && (Math.round(val) === val);
      break;
    case 'number':
      // Coerce the value only for Swagger 1.2
      if (version === '1.2' && _.isString(val)) {
        val = Number(val);
      }

      result = _.isFinite(val);
      break;
    case 'string':
      if (!_.isUndefined(format)) {
        switch (format) {
        case 'date':
          result = isValidDate(val);
          break;
        case 'date-time':
          result = isValidDateTime(val);
          break;
        }
      }
      break;
    case 'void':
      result = _.isUndefined(val);
      break;
    }
  }

  if (skipError) {
    return result;
  } else if (!result) {
    throwErrorWithCode('INVALID_TYPE',
                       type !== 'void' ?
                         'Not a valid ' + (_.isUndefined(format) ? '' : format + ' ') + type + ': ' + oVal :
                         'Void does not allow a value');
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.swagger-tools.validators.validateUniqueItems"></a>[function <span class="apidocSignatureSpan">swagger-tools.validators.</span>validateUniqueItems (val, isUnique)](#apidoc.element.swagger-tools.validators.validateUniqueItems)
- description and source-code
```javascript
validateUniqueItems = function (val, isUnique) {
  if (!_.isUndefined(isUnique) && _.uniq(val).length !== val.length) {
    throwErrorWithCode('ARRAY_UNIQUE', 'Does not allow duplicate values: ' + val.join(', '));
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
