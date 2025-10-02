## Why
Some operators (_e.g._ `with_latest_from` were not compiling), and some recent performance changes (_i.e._ [PR562](https://github.com/ReactiveX/RxCpp/pull/562) and [PR564](https://github.com/ReactiveX/RxCpp/pull/564)) were not brought in from the [`v4.1.1`](https://github.com/ReactiveX/RxCpp/releases/tag/v4.1.1) release that the official `vcpkg` port uses. So we forked the `latest` version from `RxCpp` and brought in some extra changes that were needed.

> This required some codebase updates, as `just` operator now moves its ctor input, and `map` assumes that the input value will not be transformed (_i.e._ is const/not a reference).

## Changes
  - [x] changed project name to align w/ our `vcpkg` port name (_i.e._ `rxcpp-moverse`)
  - [x] applied the change from this [comment](https://github.com/YousicianGit/RxCpp/pull/1/files#r1087751714) from Yousician's [PR](https://github.com/YousicianGit/RxCpp/pull/1/files).     