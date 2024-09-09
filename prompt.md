I would like that you generate a devfile following the structure below:

```yaml
schemaVersion: 2.0.0
components:
  - name: dev 
    container:
      image: public.ecr.aws/aws-mde/universal-image:latest
commands:
  - id: test 
    exec:
      component: dev
      commandLine: "python3.11 manage.py test"
  - id: make_migrations 
    exec:
      component: dev
      commandLine: "python3.11 manage.py makemigrations"
  - id: install 
    exec:
      component: dev 
      commandLine: "pip3.11 install -r requirements.txt"
```
If you have doubts about the commands, you can check the documentation on the following link: https://devfile.io/docs/2.3.0/what-is-a-devfile

But rebuild using the commands included on /Users/tverney/Desktop/Development/sites/jewelryecommerce/package.json scripts.