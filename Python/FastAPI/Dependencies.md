
FastAPI depends on Pydantic and Starlette.

### Standard Dependencies

When you install FastAPI with `pip install "fastapi[standard]"` it comes the `standard` group of optional dependencies:

Used by Pydantic:

- [`email-validator`]- for email validation.

Used by Starlette:

- [`httpx`] - Required if you want to use the `TestClient`.
- [`jinja2`]- Required if you want to use the default template configuration.
- [`python-multipart`]- Required if you want to support form "parsing", with `request.form()`.

Used by FastAPI / Starlette:

- [`uvicorn`] - for the server that loads and serves your application. This includes `uvicorn[standard]`, which includes some dependencies (e.g. `uvloop`) needed for high performance serving.
- `fastapi-cli` - to provide the `fastapi` command.

### Without Standard Dependencies

If you don't want to include the `standard` optional dependencies, you can install with `pip install fastapi` instead of `pip install "fastapi[standard]"`.

### Additional Optional Dependencies

There are some additional dependencies you might want to install.

Additional optional Pydantic dependencies:

- [`pydantic-settings`](https://docs.pydantic.dev/latest/usage/pydantic_settings/)- for settings management.
- [`pydantic-extra-types`](https://docs.pydantic.dev/latest/usage/types/extra_types/extra_types/) - for extra types to be used with Pydantic.

Additional optional FastAPI dependencies:

- [`orjson`](https://github.com/ijl/orjson) - Required if you want to use `ORJSONResponse`.
- [`ujson`](https://github.com/esnme/ultrajson) - Required if you want to use `UJSONResponse`.