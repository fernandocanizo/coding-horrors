# Useless

Yeah! Let's make a function, with all the associated overload when calling it, to just return the parameter we already had:

```ts
export const buildPathName = ({
  section,
  withSearchParams = false,
  customUrl = null,
  groupId,
  rowsPerPage = "25",
}: {
  section: ContextView
  withSearchParams?: boolean
  customUrl?: string | null
  groupId?: string | null
  rowsPerPage?: string
}) => {
  if (customUrl) return customUrl
  // ...
```

Why on Earth would you add a parameter to a function that if provided just returns the very same parameter unchanged?
