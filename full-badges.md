
# Notes on adding badges for rOpenSci repos

Start with package name on line 1 with a top level markdown heading

```
# Package Name
```

## Badges

Badges should reflect a level of trust (repo status + review status), build quality (Travis, Appveyor, code coverage), publishing stats (version on CRAN, Monthly downloads, and Zenodo DOI).

**Line 1**

Start with rOpenSci review status. Can be under review, or accepted.

[![](https://img.shields.io/badge/-Under_Review-yellow.svg?style=flat-square&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz48c3ZnIHZlcnNpb249IjEuMSIgaWQ9IkxheWVyXzEiIHg9IjBweCIgeT0iMHB4IiB2aWV3Qm94PSIyNy4xOTI5ODIxOTY4MDc4NiAxMC4xOTczNjg2MjE4MjYxNzIgMjAzLjk0NzM1Mjg4NjE5OTk1IDIxMi4xMTY2Njg3MDExNzE4OCIgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgNzc1IDI3Ni43OyIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gIDxzdHlsZSB0eXBlPSJ0ZXh0L2NzcyI%2BLnN0MHtmaWxsOiMxQTFBMUE7fTwvc3R5bGU%2BICA8ZyB0cmFuc2Zvcm09Im1hdHJpeCgxLCAwLCAwLCAxLCA1LjY2NTIwNSwgMCkiPiAgICA8Zz4gICAgICA8cGF0aCBjbGFzcz0ic3QwIiBkPSJNMTI2LjcsNjIuNWMwLTE3LjEtMTAuNC0zMS44LTI1LjItMzguMWMtNS0yLjEtMTAuNC0zLjMtMTYuMS0zLjNIMzYuN2gtMC4xbDAuMSwxMTUuMmgyNS4xdi0zMi41aDE4LjYmIzEwOyYjOTsmIzk7JiM5O2wxNS45LDMyLjVoMjcuNGwtMTguOC0zNy40QzExNy45LDkxLjksMTI2LjcsNzguMiwxMjYuNyw2Mi41eiBNMTAxLjYsNjIuNWMwLDktNy4zLDE2LjMtMTYuMywxNi4zSDYxLjhWNDYuMmgyMy41JiMxMDsmIzk7JiM5OyYjOTtDOTQuMyw0Ni4yLDEwMS42LDUzLjUsMTAxLjYsNjIuNXoiIHN0eWxlPSJmaWxsOiByZ2IoMjMwLCAyMzAsIDIzMCk7Ii8%2BICAgICAgPHBhdGggY2xhc3M9InN0MCIgZD0iTTE1Ny45LDk5LjR2LTguOUwxMzYuNiwxMTBsMjEuMywyMC40di04LjljMjAuMywwLDMyLjQsMTcuNiwzMi40LDM1LjVjMCwxNy45LTEyLjUsMzYuMS0zMi40LDM2LjEmIzEwOyYjOTsmIzk7JiM5O2MtMjEuNiwwLTMyLjQtMTguMi0zMi40LTM2LjFoLTI1LjJjMCwzMS44LDI1LjgsNTcuNiw1Ny42LDU3LjZjMzEuOCwwLDU3LjYtMjUuOCw1Ny42LTU3LjZDMjE1LjYsMTI1LjEsMTg5LjgsOTkuNCwxNTcuOSw5OS40eiIgc3R5bGU9ImZpbGw6IHJnYigyMzAsIDIzMCwgMjMwKTsiLz4gICAgPC9nPiAgPC9nPjwvc3ZnPg%3D%3D)](https://www.ropensci.org)

[![](https://img.shields.io/badge/-Peer_Reviewed-brightgreen.svg?style=flat-square&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz48c3ZnIHZlcnNpb249IjEuMSIgaWQ9IkxheWVyXzEiIHg9IjBweCIgeT0iMHB4IiB2aWV3Qm94PSIyNy4xOTI5ODIxOTY4MDc4NiAxMC4xOTczNjg2MjE4MjYxNzIgMjAzLjk0NzM1Mjg4NjE5OTk1IDIxMi4xMTY2Njg3MDExNzE4OCIgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgNzc1IDI3Ni43OyIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4gIDxzdHlsZSB0eXBlPSJ0ZXh0L2NzcyI%2BLnN0MHtmaWxsOiMxQTFBMUE7fTwvc3R5bGU%2BICA8ZyB0cmFuc2Zvcm09Im1hdHJpeCgxLCAwLCAwLCAxLCA1LjY2NTIwNSwgMCkiPiAgICA8Zz4gICAgICA8cGF0aCBjbGFzcz0ic3QwIiBkPSJNMTI2LjcsNjIuNWMwLTE3LjEtMTAuNC0zMS44LTI1LjItMzguMWMtNS0yLjEtMTAuNC0zLjMtMTYuMS0zLjNIMzYuN2gtMC4xbDAuMSwxMTUuMmgyNS4xdi0zMi41aDE4LjYmIzEwOyYjOTsmIzk7JiM5O2wxNS45LDMyLjVoMjcuNGwtMTguOC0zNy40QzExNy45LDkxLjksMTI2LjcsNzguMiwxMjYuNyw2Mi41eiBNMTAxLjYsNjIuNWMwLDktNy4zLDE2LjMtMTYuMywxNi4zSDYxLjhWNDYuMmgyMy41JiMxMDsmIzk7JiM5OyYjOTtDOTQuMyw0Ni4yLDEwMS42LDUzLjUsMTAxLjYsNjIuNXoiIHN0eWxlPSJmaWxsOiByZ2IoMjMwLCAyMzAsIDIzMCk7Ii8%2BICAgICAgPHBhdGggY2xhc3M9InN0MCIgZD0iTTE1Ny45LDk5LjR2LTguOUwxMzYuNiwxMTBsMjEuMywyMC40di04LjljMjAuMywwLDMyLjQsMTcuNiwzMi40LDM1LjVjMCwxNy45LTEyLjUsMzYuMS0zMi40LDM2LjEmIzEwOyYjOTsmIzk7JiM5O2MtMjEuNiwwLTMyLjQtMTguMi0zMi40LTM2LjFoLTI1LjJjMCwzMS44LDI1LjgsNTcuNiw1Ny42LDU3LjZjMzEuOCwwLDU3LjYtMjUuOCw1Ny42LTU3LjZDMjE1LjYsMTI1LjEsMTg5LjgsOTkuNCwxNTcuOSw5OS40eiIgc3R5bGU9ImZpbGw6IHJnYigyMzAsIDIzMCwgMjMwKTsiLz4gICAgPC9nPiAgPC9nPjwvc3ZnPg%3D%3D)](https://www.ropensci.org)

- Be sure that the link goes to the review thread and not to ropensci.org

If a package percedes onboarding or was added directly, skip to the repostatus badges:

Concept - for early stage projects

[![Project Status: Concept – Minimal or no implementation has been done yet, or the repository is only intended to be a limited example, demo, or proof-of-concept.](http://www.repostatus.org/badges/latest/concept.svg)](http://www.repostatus.org/#concept)

WIP - For projects that are not yet installable but have progressed beyond a concept


[![Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.](http://www.repostatus.org/badges/latest/wip.svg)](http://www.repostatus.org/#wip)

Suspended - Work stopped for various reasons

[![Project Status: Suspended – Initial development has started, but there has not yet been a stable, usable release; work has been stopped for the time being but the author(s) intend on resuming work.](http://www.repostatus.org/badges/latest/suspended.svg)](http://www.repostatus.org/#suspended)

Abandoned: No further development planned

[![Project Status: Abandoned – Initial development has started, but there has not yet been a stable, usable release; the project has been abandoned and the author(s) do not intend on continuing development.](http://www.repostatus.org/badges/latest/abandoned.svg)](http://www.repostatus.org/#abandoned)

Active - This will be our most used badge

[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)

Inactive - Maintainer plans no further updates

[![Project Status: Inactive – The project has reached a stable, usable state but is no longer being actively developed; support/maintenance will be provided as time allows.](http://www.repostatus.org/badges/latest/inactive.svg)](http://www.repostatus.org/#inactive)

Unsupported: Seeking a new maintainer


[![Project Status: Unsupported – The project has reached a stable, usable state but the author(s) have ceased all work on it. A new maintainer may be desired.](http://www.repostatus.org/badges/latest/unsupported.svg)](http://www.repostatus.org/#unsupported)

**Line 2**

Appveyor - Use `use_appveyor` to get code  
Travis - Use `use_travis` to get code  
Coverage - Use `use_coverage` to get code  


**Line 3**

CRAN version  
CRAN monthly downloads  
Zenodo DOI  


