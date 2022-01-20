def snakeCaseToCamelCase(snake_case: str) -> str:

"""

Convert snake case str to camel case

"""

first, *others = snake_case.split("_")

return "".join([first.lower(), *map(str.title, others)])