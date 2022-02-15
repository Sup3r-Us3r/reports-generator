# ReportsGenerator

## Run app

Install dependencies

```bash
$ mix deps.get
```

Run tests

```bash
$ mix test
```

Run normal version

```bash
$ iex -S mix

iex> ReportsGenerator.build("report_complete.csv")
```

Run with parallel version

```bash
$ iex -S mix

iex> ReportsGenerator.build_from_many(["report_1.csv", "report_2.csv", "report_3.csv"])
```

Get runtime from normal version

```bash
$ iex -S mix

iex> :timer.tc(fn -> ReportsGenerator.build("report_complete.csv") end)
```

Get runtime from parallel version

```bash
$ iex -S mix

iex> :timer.tc(fn -> ReportsGenerator.build_from_many(["report_1.csv", "report_2.csv", "report_3.csv"]) end)
```
