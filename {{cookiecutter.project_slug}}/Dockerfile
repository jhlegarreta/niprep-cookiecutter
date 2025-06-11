FROM python:{{ cookiecutter.python }}-slim

COPY . /opt/{{ cookiecutter.project_slug }}
WORKDIR /opt/{{ cookiecutter.project_slug }}

RUN pip install .

ENTRYPOINT ["{{ cookiecutter.project_slug }}"]
