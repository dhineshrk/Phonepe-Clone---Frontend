<template>
  <!--Container Section-->
  <section class="mx-auto bg-white h-20 flex lg:items-center lg:justify-center lg:w-8/12">
    <!--Small screen logo and button-->

    <div class="flex items-center sm:px-10 sm:justify-between sm:w-screen">
      <img class="h-14 py-2" src="data:image/svg+xml;base64,PHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSJMYXllcl8yIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHg9IjAiIHk9IjAiIHZpZXdCb3g9IjAgMCAxMzIgNDgiIHhtbDpzcGFjZT0icHJlc2VydmUiPjxzdHlsZT4uc3Qwe2ZpbGw6IzVmMjU5Zn08L3N0eWxlPjxjaXJjbGUgdHJhbnNmb3JtPSJyb3RhdGUoLTc2LjcxNCAxNy44NyAyNC4wMDEpIiBjbGFzcz0ic3QwIiBjeD0iMTcuOSIgY3k9IjI0IiByPSIxNy45Ii8+PHBhdGggY2xhc3M9InN0MCIgZD0iTTkwLjUgMzQuMnYtNi41YzAtMS42LS42LTIuNC0yLjEtMi40LS42IDAtMS4zLjEtMS43LjJWMzVjMCAuMy0uMy42LS42LjZoLTIuM2MtLjMgMC0uNi0uMy0uNi0uNlYyMy45YzAtLjQuMy0uNy42LS44IDEuNS0uNSAzLS44IDQuNi0uOCAzLjYgMCA1LjYgMS45IDUuNiA1LjR2Ny40YzAgLjMtLjMuNi0uNi42SDkyYy0uOSAwLTEuNS0uNy0xLjUtMS41em05LTMuOWwtLjEuOWMwIDEuMi44IDEuOSAyLjEgMS45IDEgMCAxLjktLjMgMi45LS44LjEgMCAuMi0uMS4zLS4xLjIgMCAuMy4xLjQuMi4xLjEuMy40LjMuNC4yLjMuNC43LjQgMSAwIC41LS4zIDEtLjcgMS4yLTEuMS42LTIuNC45LTMuOC45LTEuNiAwLTIuOS0uNC0zLjktMS4yLTEtLjktMS42LTIuMS0xLjYtMy42di0zLjljMC0zLjEgMi01IDUuNC01IDMuMyAwIDUuMiAxLjggNS4yIDV2Mi40YzAgLjMtLjMuNi0uNi42aC02LjN6bS0uMS0yLjJIMTAzLjJ2LTFjMC0xLjItLjctMi0xLjktMnMtMS45LjctMS45IDJ2MXptMjUuNSAyLjJsLS4xLjljMCAxLjIuOCAxLjkgMi4xIDEuOSAxIDAgMS45LS4zIDIuOS0uOC4xIDAgLjItLjEuMy0uMS4yIDAgLjMuMS40LjIuMS4xLjMuNC4zLjQuMi4zLjQuNy40IDEgMCAuNS0uMyAxLS43IDEuMi0xLjEuNi0yLjQuOS0zLjguOS0xLjYgMC0yLjktLjQtMy45LTEuMi0xLS45LTEuNi0yLjEtMS42LTMuNnYtMy45YzAtMy4xIDItNSA1LjQtNSAzLjMgMCA1LjIgMS44IDUuMiA1djIuNGMwIC4zLS4zLjYtLjYuNmgtNi4zem0tLjEtMi4ySDEyOC42di0xYzAtMS4yLS43LTItMS45LTJzLTEuOS43LTEuOSAydjF6TTY2IDM1LjdoMS40Yy4zIDAgLjYtLjMuNi0uNnYtNy40YzAtMy40LTEuOC01LjQtNC44LTUuNC0uOSAwLTEuOS4yLTIuNS40VjE5YzAtLjgtLjctMS41LTEuNS0xLjVoLTEuNGMtLjMgMC0uNi4zLS42LjZ2MTdjMCAuMy4zLjYuNi42aDIuM2MuMyAwIC42LS4zLjYtLjZ2LTkuNGMuNS0uMiAxLjItLjMgMS43LS4zIDEuNSAwIDIuMS43IDIuMSAyLjR2Ni41Yy4xLjcuNyAxLjQgMS41IDEuNHptMTUuMS04LjRWMzFjMCAzLjEtMi4xIDUtNS42IDUtMy40IDAtNS42LTEuOS01LjYtNXYtMy43YzAtMy4xIDIuMS01IDUuNi01IDMuNSAwIDUuNiAxLjkgNS42IDV6bS0zLjUgMGMwLTEuMi0uNy0yLTItMnMtMiAuNy0yIDJWMzFjMCAxLjIuNyAxLjkgMiAxLjlzMi0uNyAyLTEuOXYtMy43em0tMjIuMy0xLjdjMCAzLjItMi40IDUuNC01LjYgNS40LS44IDAtMS41LS4xLTIuMi0uNHY0LjVjMCAuMy0uMy42LS42LjZoLTIuM2MtLjMgMC0uNi0uMy0uNi0uNlYxOS4yYzAtLjQuMy0uNy42LS44IDEuNS0uNSAzLS44IDQuNi0uOCAzLjYgMCA2LjEgMi4yIDYuMSA1LjZ2Mi40ek01MS43IDIzYzAtMS42LTEuMS0yLjQtMi42LTIuNC0uOSAwLTEuNS4zLTEuNS4zdjYuNmMuNi4zLjkuNCAxLjYuNCAxLjUgMCAyLjYtLjkgMi42LTIuNFYyM3ptNjguMiAyLjZjMCAzLjItMi40IDUuNC01LjYgNS40LS44IDAtMS41LS4xLTIuMi0uNHY0LjVjMCAuMy0uMy42LS42LjZoLTIuM2MtLjMgMC0uNi0uMy0uNi0uNlYxOS4yYzAtLjQuMy0uNy42LS44IDEuNS0uNSAzLS44IDQuNi0uOCAzLjYgMCA2LjEgMi4yIDYuMSA1LjZ2Mi40em0tMy42LTIuNmMwLTEuNi0xLjEtMi40LTIuNi0yLjQtLjkgMC0xLjUuMy0xLjUuM3Y2LjZjLjYuMy45LjQgMS42LjQgMS41IDAgMi42LS45IDIuNi0yLjRWMjN6Ii8+PHBhdGggZD0iTTI2IDE5LjNjMC0uNy0uNi0xLjMtMS4zLTEuM2gtMi40bC01LjUtNi4zYy0uNS0uNi0xLjMtLjgtMi4xLS42bC0xLjkuNmMtLjMuMS0uNC41LS4yLjdsNiA1LjdIOS41Yy0uMyAwLS41LjItLjUuNXYxYzAgLjcuNiAxLjMgMS4zIDEuM2gxLjR2NC44YzAgMy42IDEuOSA1LjcgNS4xIDUuNyAxIDAgMS44LS4xIDIuOC0uNXYzLjJjMCAuOS43IDEuNiAxLjYgMS42aDEuNGMuMyAwIC42LS4zLjYtLjZWMjAuOGgyLjNjLjMgMCAuNS0uMi41LS41di0xem0tNi40IDguNmMtLjYuMy0xLjQuNC0yIC40LTEuNiAwLTIuNC0uOC0yLjQtMi42di00LjhoNC40djd6IiBmaWxsPSIjZmZmIi8+PC9zdmc+" alt="">
      <div class="lg:hidden flex sm:ml-auto"><img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjgiIGhlaWdodD0iMjMiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PGcgc3Ryb2tlPSIjNjYzQUI1IiBzdHJva2Utd2lkdGg9IjIiIGZpbGw9Im5vbmUiIGZpbGwtcnVsZT0iZXZlbm9kZCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIj48cGF0aCBkPSJNMS40MTQgMS4zNTNoMjQuODZNMS40MTQgMTEuMjI4aDI0Ljg2TTEuNDE0IDIxLjQ1N2gyNC44NiIvPjwvZz48L3N2Zz4=" alt=""></div>
    </div>

    <!--Small screen logo and button End-->

      <div class="hidden lg:flex lg:items-center text-black">
        <div class="font-bold px-8 hover:text-purple-500"><a href="#">BUSINESS SOLUTIONS</a></div>
        <div class="font-bold px-8 hover:text-purple-500"><a href="#">PRESS</a></div>
        <div class="font-bold px-8 hover:text-purple-500"><a href="#">CAREERS</a></div>
        <div class="font-bold px-8 hover:text-purple-500"><a href="#">ABOUT US</a></div>
        <div class="font-bold px-8 hover:text-purple-500"><a href="#">BLOG</a></div>
        <div class="font-bold px-8 hover:text-purple-500"><a href="#">CONTACT US</a></div>
        <div class="font-bold px-8 hover:text-purple-500"><a href="#">TRUST & SAFETY</a></div>
      </div>
  </section>

  <!--Second Container-->
  <section class="bg-purple-100 h-16 flex items-center justify-center  sm:sticky sm:top-0">

    <div class="lg:w-7/12 flex justify-between ">

      <div class="flex sm:justify-between sm:items-center sm:w-screen sm:px-10 ">

        <div class="text-purple-500 font-semibold"><a href="#">Payment Gateway</a></div>
        <div class="ms-auto lg:hidden">
          <img  src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTMiIGhlaWdodD0iOCIgdmlld0JveD0iMCAwIDEzIDgiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxwYXRoIGQ9Ik0yLjAzOTA2IDIuMDAzOTFMNi42NzQyNyA2LjQ3ODhMMTEuMDc1NyAxLjk2MjU1IiBzdHJva2U9IiM1RTJCOUQiIHN0cm9rZS13aWR0aD0iMi41IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==" alt="">
      </div>
    </div>

      <div class="hidden lg:flex lg:items-center sm:justify-between z-1">
        <div class="flex">
          <div class="text-black px-5  hover:text-purple-500"><a href="#">Solutions</a></div>
          <div class="text-black px-5  hover:text-purple-500"><a href="#">Pricing</a></div>
          <div class="text-black px-5  hover:text-purple-500"><a href="#">Plugins</a></div>
          <div class="text-black px-5  hover:text-purple-500"><a href="#">Developers</a></div>
          <div class="text-black px-5  hover:text-purple-500"><a href="#">Resources</a></div>
          <div class="text-black px-5  hover:text-purple-500"><a href="#">FAQs</a></div>
      </div>
      </div>
    </div>
</section>
<!--End of Second Container-->




<div class="lg:flex lg:items-top lg:mt-20 lg:justify-center">
  <div class="flex sm:flex-col sm:text-center lg:w-1/2 lg:items-center ">
    <img class="sm:h-9 mt-8 flex sm:justify-center sm:items-center sm:w-full" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjU2IiBoZWlnaHQ9IjU1IiB2aWV3Qm94PSIwIDAgMjU2IDU1IiBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPgo8cGF0aCBkPSJNMC42NjQwNjIgMjcuNjIwMUMwLjY2NDA2MiAxMi43OTI2IDEyLjcwOTIgMC43NzM0MzggMjcuNTY4NiAwLjc3MzQzOEM0Mi40MjgzIDAuNzczNDM4IDU0LjQ3MzYgMTIuNzkyNiA1NC40NzM2IDI3LjYyMDFDNTQuNDczNiA0Mi40NDc2IDQyLjQyODMgNTQuNDY2OCAyNy41Njg2IDU0LjQ2NjhDMTIuNzEzMiA1NC40NjY4IDAuNjY0MDYyIDQyLjQ0NzYgMC42NjQwNjIgMjcuNjIwMVoiIGZpbGw9IiM1RjI1OUYiLz4KPHBhdGggZD0iTTM5Ljc0NiAyMC41ODA4QzM5Ljc0NiAxOS41NDE1IDM4Ljg5OTUgMTguNjk2NiAzNy44NTgyIDE4LjY5NjZIMzQuMjcyNEwyNi4wMDM3IDkuMTc2NzZDMjUuMjM2NCA4LjI5MjA3IDI0LjAyNCA3LjkzODkyIDIyLjkwMyA4LjI3MTk5TDIwLjAzMjggOS4xMjQ5M0MxOS41OTU1IDkuMjU1OSAxOS40NjA0IDkuODExMTUgMTkuNzkwMyAxMC4xMjQ1TDI4Ljc5NDQgMTguNjkyOUgxNS4wMzU5QzE0LjYzODMgMTguNjkyOSAxNC4zMjAzIDE5LjAxNCAxNC4zMjAzIDE5LjQwNjlWMjAuOTU3N0MxNC4zMjAzIDIxLjk5NzEgMTUuMTYzMSAyMi44NDIgMTYuMjA4NiAyMi44NDJIMTguMzExNVYzMC4wODlDMTguMzExNSAzNS41IDIxLjIwMTUgMzguNzI4NSAyNi4wMzk1IDM4LjcyODVDMjcuNTEwMyAzOC43Mjg1IDI4Ljc3NDMgMzguNTU4MiAzMC4yMjU0IDM3Ljk5MDlWNDIuODIyNUMzMC4yMjU0IDQ0LjEzMTUgMzEuMjkwOSA0NS4xOTQ1IDMyLjYwMjcgNDUuMTk0NUgzNC42ODk4QzM1LjE4NjQgNDUuMTk0NSAzNS41ODgyIDQ0Ljc5NCAzNS41ODgyIDQ0LjI5NzhWMjIuODQySDM5LjAzODVDMzkuNDM2MyAyMi44NDIgMzkuNzU0MSAyMi41MjA2IDM5Ljc1NDEgMjIuMTI4VjIwLjU4MDhIMzkuNzQ2Wk0zMC4yMTc0IDMzLjQ4MDdDMjkuMzcwOSAzMy44NjE2IDI4LjEzODMgMzQuMDc1NyAyNy4yMjc5IDM0LjA3NTdDMjQuNzYzNCAzNC4wNzU3IDIzLjY2NjIgMzIuODQ1OSAyMy42NjYyIDMwLjA5M1YyMi44NDZIMzAuMjE3NFYzMy40ODA3WiIgZmlsbD0id2hpdGUiLz4KPHBhdGggZD0iTTEzNi44ODYgNDIuOTU5NVYzMy4yMDk1QzEzNi44ODYgMzAuNzUzOSAxMzUuOTIgMjkuNjU5MSAxMzMuNzU3IDI5LjY1OTFDMTMyLjgzOSAyOS42NTkxIDEzMS44MDEgMjkuNzgyIDEzMS4xMzQgMzAuMDEyMlY0NC4zMDAyQzEzMS4xMzQgNDQuNzk2IDEzMC43MzIgNDUuMTk2OSAxMzAuMjM1IDQ1LjE5NjlIMTI2Ljc5M0MxMjYuMyA0NS4xOTY5IDEyNS44OTQgNDQuNzk2IDEyNS44OTQgNDQuMzAwMlYyNy41Njg3QzEyNS44OTQgMjYuOTg1NyAxMjYuMjg4IDI2LjQ4MTkgMTI2Ljc1NyAyNi4zMTUyQzEyOC45NzkgMjUuNTI1NyAxMzEuMzIgMjUuMDQ1NiAxMzMuNzUzIDI1LjA0NTZDMTM5LjE2OCAyNS4wNDU2IDE0Mi4xNTMgMjcuOTQ1NiAxNDIuMTUzIDMzLjIxMzVWNDQuMzA0MkMxNDIuMTUzIDQ0LjggMTQxLjc1MSA0NS4yMDA5IDE0MS4yNTUgNDUuMjAwOUgxMzkuMTI0QzEzNy44ODggNDUuMTk2OSAxMzYuODg2IDQ0LjE5MzMgMTM2Ljg4NiA0Mi45NTk1Wk0xNTAuNDYxIDM3LjA3NjlIMTUwLjM0MlYzNy4xOTU4TDE1MC4zNDYgMzguNDU3M0MxNTAuMzQ2IDQwLjI4MjEgMTUxLjUxMSA0MS4zMjkxIDE1My41NDIgNDEuMzI5MUMxNTUuMDQ5IDQxLjMyOTEgMTU2LjQ4IDQwLjk0ODMgMTU3LjkwNyA0MC4xNjI4QzE1Ny45OTEgNDAuMTE5NCAxNTguMTQyIDQwLjA1NTkgMTU4LjM4NCA0MC4wNTU5QzE1OC42NjcgNDAuMDU1OSAxNTguODk3IDQwLjIxODcgMTU5LjAyOCA0MC4zNzMzQzE1OS4xNjMgNDAuNTI4IDE1OS41NTMgNDAuOTggMTU5LjU1MyA0MC45OEMxNTkuOTI2IDQxLjQxMjcgMTYwLjE1NyA0MS45Njc5IDE2MC4xMzcgNDIuNTM5MkMxNjAuMTA5IDQzLjMxMjYgMTU5LjY5MiA0My45ODI4IDE1OS4wNCA0NC4zMjc5QzE1Ny4zNTEgNDUuMjI0NiAxNTUuNDk0IDQ1LjY2MDkgMTUzLjM2MyA0NS42NjA5QzE1MC45OSA0NS42NjA5IDE0OC45NTkgNDUuMDMwMiAxNDcuNDg4IDQzLjgzMjFDMTQ1LjkwNiA0Mi41NDY5IDE0NS4wNzEgNDAuNjUxIDE0NS4wNzEgMzguMzVWMzIuNTI2OUMxNDUuMDcxIDI3LjgzODMgMTQ4LjEzMiAyNS4wMzggMTUzLjI1NiAyNS4wMzhDMTU4LjI1MyAyNS4wMzggMTYxLjExOSAyNy43NjcyIDE2MS4xMTkgMzIuNTI2OUwxNjEuMTE1IDM2LjE4MDVDMTYxLjExNSAzNi42NzIzIDE2MC43MTQgMzcuMDcyOCAxNjAuMjE3IDM3LjA3MjhIMTUwLjQ2MVYzNy4wNzY5Wk0xNTAuMzQyIDMzLjc4MDRIMTUwLjQ2MUgxNTUuOTcxSDE1Ni4wOVYzMy42NjE1TDE1Ni4wOTQgMzIuMjgxQzE1Ni4wOTQgMzAuNDEyOCAxNTUuMDQ1IDI5LjMzNzcgMTUzLjIyIDI5LjMzNzdDMTUxLjM2NCAyOS4zMzc3IDE1MC4zNDIgMzAuMzg1MSAxNTAuMzQyIDMyLjI4MUwxNTAuMzM4IDMzLjY2MTVMMTUwLjM0MiAzMy43ODA0Wk0xODguNzY3IDM3LjA3NjlIMTg4LjY0OFYzNy4xOTU4TDE4OC42NTIgMzguNDU3M0MxODguNjUyIDQwLjI4MjEgMTg5LjgxNyA0MS4zMjkxIDE5MS44NTIgNDEuMzI5MUMxOTMuMzU5IDQxLjMyOTEgMTk0Ljc5IDQwLjk0ODMgMTk2LjIxNyA0MC4xNjI4QzE5Ni4zMDEgNDAuMTE5NCAxOTYuNDUyIDQwLjA1NTkgMTk2LjY5NCA0MC4wNTU5QzE5Ni45NzIgNDAuMDU1OSAxOTcuMjAzIDQwLjIxODcgMTk3LjMzOCA0MC4zNzMzQzE5Ny40NzMgNDAuNTI4IDE5Ny44NjMgNDAuOTggMTk3Ljg2MyA0MC45OEMxOTguMjM2IDQxLjQxMjcgMTk4LjQ2NyA0MS45Njc5IDE5OC40NDcgNDIuNTM5MkMxOTguNDE5IDQzLjMxMjYgMTk4LjAwMiA0My45ODI4IDE5Ny4zNSA0NC4zMjc5QzE5NS42NjQgNDUuMjI0NiAxOTMuODA0IDQ1LjY2MDkgMTkxLjY3MyA0NS42NjA5QzE4OS4zIDQ1LjY2MDkgMTg3LjI2OSA0NS4wMzAyIDE4NS43OTggNDMuODMyMUMxODQuMjE2IDQyLjU0NjkgMTgzLjM4MSA0MC42NTEgMTgzLjM4MSAzOC4zNVYzMi41MjY5QzE4My4zODEgMjcuODM4MyAxODYuNDQyIDI1LjAzOCAxOTEuNTY2IDI1LjAzOEMxOTYuNTYzIDI1LjAzOCAxOTkuNDI5IDI3Ljc2NzIgMTk5LjQyOSAzMi41MjY5TDE5OS40MjUgMzYuMTgwNUMxOTkuNDI1IDM2LjY3MjMgMTk5LjAyMyAzNy4wNzI4IDE5OC41MjcgMzcuMDcyOEgxODguNzY3VjM3LjA3NjlaTTE4OC42NDggMzMuNzgwNEgxODguNzY3SDE5NC4yODFIMTk0LjRWMzMuNjYxNUwxOTQuNDA0IDMyLjI4MUMxOTQuNDA0IDMwLjQxMjggMTkzLjM1NSAyOS4zMzc3IDE5MS41MyAyOS4zMzc3QzE4OS42NzQgMjkuMzM3NyAxODguNjUyIDMwLjM4NTEgMTg4LjY1MiAzMi4yODFMMTg4LjY0OCAzMy42NjE1VjMzLjc4MDRaTTEwMC4xMTggNDUuMTk2OUgxMDIuMjQ5QzEwMi43NDYgNDUuMTk2OSAxMDMuMTQ4IDQ0Ljc5NiAxMDMuMTQ4IDQ0LjMwMDJWMzMuMTczN0MxMDMuMTQ4IDI4LjA4MDYgMTAwLjQyNCAyNS4wNDIgOTUuODYwOCAyNS4wNDJDOTQuNDg1NSAyNS4wNDIgOTMuMDAyNiAyNS4yNzk5IDkyLjEyNCAyNS42NjQ3VjIwLjE3MDZDOTIuMTI0IDE4LjkzNzIgOTEuMTIyNCAxNy45MzM2IDg5Ljg4MjEgMTcuOTMzNkg4Ny43ODY5Qzg3LjI5MDMgMTcuOTMzNiA4Ni44ODg2IDE4LjMzNDEgODYuODg4NiAxOC44Mjk5VjQ0LjMwMDJDODYuODg4NiA0NC43OTYgODcuMjkwMyA0NS4xOTY5IDg3Ljc4NjkgNDUuMTk2OUg5MS4yMjU2QzkxLjcyMjYgNDUuMTk2OSA5Mi4xMjQgNDQuNzk2IDkyLjEyNCA0NC4zMDAyVjMwLjEyNzFDOTIuODM5NSAyOS44MDIxIDkzLjg4OTMgMjkuNjIzMyA5NC43MTYxIDI5LjYyMzNDOTYuOTAyNSAyOS42MjMzIDk3Ljg4MDQgMzAuNzE4MSA5Ny44ODA0IDMzLjE3MzdWNDIuOTU5NUM5Ny44NzY0IDQ0LjE5MzMgOTguODgyIDQ1LjE5NjkgMTAwLjExOCA0NS4xOTY5Wk0xMjIuODI5IDMyLjYwMjRWMzguMjA3NEMxMjIuODI5IDQyLjgwNDggMTE5LjYyNSA0NS42NjA5IDExNC40NjUgNDUuNjYwOUMxMDkuMjg1IDQ1LjY2MDkgMTA2LjA2NiA0Mi44MDQ4IDEwNi4wNjYgMzguMjA3NFYzMi42MDI0QzEwNi4wNjYgMjcuOTM3NSAxMDkuMjg1IDI1LjA0MiAxMTQuNDY1IDI1LjA0MkMxMTkuNjI1IDI1LjA0MiAxMjIuODI5IDI3LjkzNzUgMTIyLjgyOSAzMi42MDI0Wk0xMTcuNTI2IDMyLjYwMjRDMTE3LjUyNiAzMC43MzQyIDExNi40MTMgMjkuNjYzMSAxMTQuNDY5IDI5LjY2MzFDMTEyLjUyNSAyOS42NjMxIDExMS40MTIgMzAuNzM0MiAxMTEuNDEyIDMyLjYwMjRWMzguMjA3NEMxMTEuNDEyIDQwLjA2IDExMi40OTcgNDEuMDc5MiAxMTQuNDY5IDQxLjA3OTJDMTE2LjQ0MSA0MS4wNzkyIDExNy41MjYgNDAuMDYgMTE3LjUyNiAzOC4yMDc0VjMyLjYwMjRaTTgzLjk3NDYgMzAuMDE2MkM4My45NjY5IDM0Ljg3OTIgODAuMzI5NCAzOC4xNDM5IDc1LjU1OTIgMzguMTQzOUM3NC4zNTQ3IDM4LjE0MzkgNzMuMzIxIDM3Ljk3MzIgNzIuMzAzMyAzNy41NzY3VjQ0LjMwMDJDNzIuMzAzMyA0NC43OTYgNzEuOTAyIDQ1LjE5NjkgNzEuNDA1IDQ1LjE5NjlINjcuODgyN0M2Ny4zODU3IDQ1LjE5NjkgNjYuOTg0NCA0NC43OTYgNjYuOTg0NCA0NC4zMDAyVjIwLjQyODVDNjYuOTg0NCAxOS43NjYgNjcuNDQ5NiAxOS4zMSA2Ny44ODI3IDE5LjE2M0M3MC4xMDA5IDE4LjQwOTcgNzIuNDI2NyAxNy45NDkzIDc0Ljc4NzggMTcuOTQ5M0M4MC4xODYzIDE3Ljk0OTMgODMuOTcxIDIxLjIyOTcgODMuOTcxIDI2LjMwNzJWMzAuMDE2Mkg4My45NzQ2Wk03OC41ODA1IDI2LjE4ODJDNzguNTgwNSAyMy44MjQzIDc2Ljk4NjMgMjIuNjIyMiA3NC42MzY4IDIyLjYyMjJDNzMuMzQxMSAyMi42MjIyIDcyLjMwMzMgMjMuMDM0OCA3Mi4zMDMzIDIzLjAzNDhWMzIuOTIzOEM3My4xMzgyIDMzLjM3OTggNzMuNzIyNCAzMy41MjY5IDc0LjY3MjUgMzMuNTI2OUM3Ni45OTAzIDMzLjUyNjkgNzguNTgwNSAzMi4yMjk2IDc4LjU4MDUgMjkuOTcyNVYyNi4xODgyWk0xODEuMTk0IDMwLjAxNjJDMTgxLjE4NiAzNC44NzkyIDE3Ny41NDkgMzguMTQzOSAxNzIuNzc5IDM4LjE0MzlDMTcxLjU3NCAzOC4xNDM5IDE3MC41NDEgMzcuOTczMiAxNjkuNTIzIDM3LjU3NjdWNDQuMzAwMkMxNjkuNTIzIDQ0Ljc5NiAxNjkuMTIxIDQ1LjE5NjkgMTY4LjYyNSA0NS4xOTY5SDE2NS4xMDJDMTY0LjYwNSA0NS4xOTY5IDE2NC4yMDQgNDQuNzk2IDE2NC4yMDQgNDQuMzAwMlYyMC40Mjg1QzE2NC4yMDQgMTkuNzY2IDE2NC42NjkgMTkuMzEgMTY1LjEwMiAxOS4xNjNDMTY3LjMyMSAxOC40MDk3IDE2OS42NDYgMTcuOTQ5MyAxNzIuMDA4IDE3Ljk0OTNDMTc3LjQwNiAxNy45NDkzIDE4MS4xOSAyMS4yMjk3IDE4MS4xOSAyNi4zMDcyVjMwLjAxNjJIMTgxLjE5NFpNMTc1LjggMjYuMTg4MkMxNzUuOCAyMy44MjQzIDE3NC4yMDYgMjIuNjIyMiAxNzEuODU2IDIyLjYyMjJDMTcwLjU2IDIyLjYyMjIgMTY5LjUyMyAyMy4wMzQ4IDE2OS41MjMgMjMuMDM0OFYzMi45MjM4QzE3MC4zNTggMzMuMzc5OCAxNzAuOTQyIDMzLjUyNjkgMTcxLjg5MiAzMy41MjY5QzE3NC4yMSAzMy41MjY5IDE3NS44IDMyLjIyOTYgMTc1LjggMjkuOTcyNVYyNi4xODgyWiIgZmlsbD0iIzVGMjU5RiIvPgo8cGF0aCBkPSJNMjM4LjkwMyAxNy44NzVIMjA2LjAzOUMyMDkuNTQ1IDIyLjQzNjYgMjExLjYzMiAyOC4xMzY5IDIxMS42MzIgMzQuMzI4OUMyMTEuNjMyIDQwLjUyMDggMjA5LjU0NSA0Ni4yMjExIDIwNi4wMzkgNTAuNzgyN0gyMzguOTAzQzI0OC4wMSA1MC43ODI3IDI1NS4zOTMgNDMuNDE2OCAyNTUuMzkzIDM0LjMyODlDMjU1LjM5MyAyNS4yNDA5IDI0OC4wMSAxNy44NzUgMjM4LjkwMyAxNy44NzVaIiBmaWxsPSIjNUYyNTlGIi8+CjxwYXRoIGQ9Ik0yMzAuMTYyIDMxLjkzMTFDMjMwLjE2MiAzNS4zNzQyIDIyNy41NzggMzcuMTY3MyAyMjQuMjk5IDM3LjE2NzNIMjIxLjgyMlY0Mi4xMjk4SDIxOC4zMjhWMjYuNzEwOUgyMjQuMjk1QzIyNy41ODIgMjYuNzE1IDIzMC4xNjIgMjguNDY4MyAyMzAuMTYyIDMxLjkzMTFaTTIyNC4wODggMzQuMDAxN0MyMjUuNDY0IDM0LjAwMTcgMjI2LjU2NSAzMy40MTA4IDIyNi41NjUgMzEuOTMxMUMyMjYuNTY1IDMwLjQ5NTIgMjI1LjQ2NCAyOS45MDQyIDIyNC4wODggMjkuOTA0MkgyMjEuODIyVjM0LjAwMTdIMjI0LjA4OFoiIGZpbGw9IiNGNEYzRjQiLz4KPHBhdGggZD0iTTIzOC4yNjcgMzMuMjU5M0gyNDQuNTUyVjQwLjUyMjRDMjQ0LjU1MiA0MS4wNDk5IDI0NC4zODEgNDEuNDUwNSAyNDMuODUzIDQxLjcwNDRDMjQzLjA1IDQyLjA2MTUgMjQyLjAzMiA0Mi4zMzkyIDI0MC4zNTggNDIuMzM5MkMyMzUuMjE0IDQyLjMzOTIgMjMxLjY0MSAzOC45NzkyIDIzMS42NDEgMzQuNDE3NkMyMzEuNjQxIDI5Ljg3NTYgMjM1LjA5MSAyNi41IDI0MC4wNjQgMjYuNUMyNDEuOTg4IDI2LjUgMjQzLjM4NyAyNi44ODA5IDI0NC4zMzggMjcuMzAxMVYzMC43NDQyQzI0My4zIDMwLjEwOTkgMjQxLjgxNyAyOS43NzI0IDI0MC4zNzggMjkuNzcyNEMyMzcuODgyIDI5Ljc3MjQgMjM1LjQyNSAzMC45OTgyIDIzNS40MjUgMzQuNDE3NkMyMzUuNDI1IDM3LjkyNDIgMjM4LjAwOSAzOS4xNSAyNDAuNjk2IDM5LjE1QzI0MC44ODcgMzkuMTUgMjQxLjA3OCAzOS4xMjk5IDI0MS4yNjggMzkuMTI5OVYzNi4yMzg0SDIzOC4yNjNWMzMuMjU5M0gyMzguMjY3WiIgZmlsbD0iI0Y0RjNGNCIvPgo8L3N2Zz4K" alt="">
    <h2 class="font-bold sm:text-xl sm:mt-3">Empower your business with</h2>
    <h1 class="mt-3 text-3xl font-bold ">PhonePe Payment Gateway</h1>
    <p class="lg:flex sm:hidden mt-3 lg:text-left">Take your business to new heights with India's most <br>
          trusted payments platform and experience <br>
            unmatched success rates.</p>
    <p class="mt-5 text-purple-700"><span class=" text-gray-500  line-through">2%</span> FREE* - Limited Period Offer</p>
    <div class="flex sm:p-3 sm:items-center sm:justify-center sm:w-svw">
      <div class="bg-purple-700 rounded-3xl items-center justify-center p-3 px-9 text-white">GET STARTED FOR FREE</div>
    </div>
  </div>
  <div class="items-center justify-center">
    <img class="lg:flex sm:hidden -z-20 relative -top-52" src="https://www.phonepe.com/webstatic/6992/static/b9cd2123c1564032822c03dbe442bb6a/6ee12/pg_top_section_mobile.png" alt="">
    <img class="sm:flex lg:hidden" src="https://www.phonepe.com/webstatic/6992/static/b9cd2123c1564032822c03dbe442bb6a/6ee12/pg_top_section_mobile.png" alt="">
  </div>
</div>

<div class="flex justify-center flex-col mb-40 gap-5">
  <h1 class="flex justify-center font-bold">Trusted By</h1>
  <marquee behavior="" direction="left" class="w-10/12 flex mx-auto" scrollamount="15" loop="100">
    <div class="flex items-center gap-9">
      <img src="https://www.phonepe.com/webstatic/6992/static/f2c8a709758d25d5a7c15a42d01c0480/b9567/mpl-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/4b5d64beb47d2c5bf9ede5f7b541039a/eb98f/irctc-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/9ba3e76eebf0bc993c3f82f65ede9f5e/3ea71/jar-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/92ced4d9689f9dffec028d6f63b8eba2/681de/confirmtkt-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/92402e28180f226ce3a1a0cf1d5e2dd8/9a8d7/pharmeasy-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/4c6602e40ecac8efa9aa075874431427/68047/dream-11-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/56ce1cfb5dc78b17ac9bfd8403466153/3ea71/meesho-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/46d5eebe474c2915094c82a1c7ed6a0c/36e58/simpl-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/403dcf5943533ed36f1f6aba20505477/d3df7/josh-talks-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/ea6e08b1b2e2a3d4b3fe9ae2e0f6cd36/9af2a/man-matters-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/60b983521b416a72042d68ab8e4d2c8a/f7da6/cashe1-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/e5725bb04e932627e05f6e3b11edfe0b/36e58/bakingo-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/bdb61f15b22aaa65e3ba8222fff943c1/37d5a/oyo-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/9b87feb51a828c9ad5dd3f1054e6e009/1ef16/airtel-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/cb2e4de6180555e3debec86c8cc94a81/30f90/zoomin-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/1e48a721250a94ec8b3c8491ea84a5f8/0f252/winni-logo.png" class="h-12" alt="">
      <img src="https://www.phonepe.com/webstatic/6992/static/86c52301fb9dbc8e805fc801510a6736/18798/branch-logo.png" class="h-12" alt="">
    </div>
  </marquee>
</div>


<div class="sm:pt-5 sm:pl-5 sm:pr-5 lg:px-60">
  <img class="ml-auto -z-40 absolute flex justify-end w-full lg:hidden" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDMxIiBoZWlnaHQ9IjU4MCIgdmlld0JveD0iMCAwIDQzMSA1ODAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIG9wYWNpdHk9IjAuNzgiPgo8ZyBmaWx0ZXI9InVybCgjZmlsdGVyMF9mXzQzNjhfOTgwMSkiPgo8ZWxsaXBzZSBjeD0iMjE3Ljc5MiIgY3k9IjIwNS41MTEiIHJ4PSIyMTcuNzkyIiByeT0iMjA1LjUxMSIgdHJhbnNmb3JtPSJtYXRyaXgoLTQuMzcxMTRlLTA4IC0xIC0xIDQuMzcxMTRlLTA4IDU3Ni4wODggNDkxLjU3MykiIGZpbGw9IiNDM0FBRjgiLz4KPC9nPgo8ZyBzdHlsZT0ibWl4LWJsZW5kLW1vZGU6bXVsdGlwbHkiIGZpbHRlcj0idXJsKCNmaWx0ZXIxX2ZfNDM2OF85ODAxKSI+CjxlbGxpcHNlIGN4PSIxNzMuMTg0IiBjeT0iMTgzLjY4IiByeD0iMTczLjE4NCIgcnk9IjE4My42OCIgdHJhbnNmb3JtPSJtYXRyaXgoLTQuMzcxMTRlLTA4IC0xIC0xIDQuMzcxMTRlLTA4IDM0OC4xNjYgNTE2LjA2MykiIGZpbGw9IiM4RURCRTUiLz4KPC9nPgo8L2c+CjxkZWZzPgo8ZmlsdGVyIGlkPSJmaWx0ZXIwX2ZfNDM2OF85ODAxIiB4PSIxMDkuNDg1IiB5PSIwLjQwNjU3IiB3aWR0aD0iNTIyLjE4NCIgaGVpZ2h0PSI1NDYuNzQ4IiBmaWx0ZXJVbml0cz0idXNlclNwYWNlT25Vc2UiIGNvbG9yLWludGVycG9sYXRpb24tZmlsdGVycz0ic1JHQiI+CjxmZUZsb29kIGZsb29kLW9wYWNpdHk9IjAiIHJlc3VsdD0iQmFja2dyb3VuZEltYWdlRml4Ii8+CjxmZUJsZW5kIG1vZGU9Im5vcm1hbCIgaW49IlNvdXJjZUdyYXBoaWMiIGluMj0iQmFja2dyb3VuZEltYWdlRml4IiByZXN1bHQ9InNoYXBlIi8+CjxmZUdhdXNzaWFuQmx1ciBzdGREZXZpYXRpb249IjI3Ljc5MDciIHJlc3VsdD0iZWZmZWN0MV9mb3JlZ3JvdW5kQmx1cl80MzY4Xzk4MDEiLz4KPC9maWx0ZXI+CjxmaWx0ZXIgaWQ9ImZpbHRlcjFfZl80MzY4Xzk4MDEiIHg9Ii0xMjIuMzgyIiB5PSI2Ni41MDgyIiB3aWR0aD0iNTczLjczNCIgaGVpZ2h0PSI1NTIuNzQxIiBmaWx0ZXJVbml0cz0idXNlclNwYWNlT25Vc2UiIGNvbG9yLWludGVycG9sYXRpb24tZmlsdGVycz0ic1JHQiI+CjxmZUZsb29kIGZsb29kLW9wYWNpdHk9IjAiIHJlc3VsdD0iQmFja2dyb3VuZEltYWdlRml4Ii8+CjxmZUJsZW5kIG1vZGU9Im5vcm1hbCIgaW49IlNvdXJjZUdyYXBoaWMiIGluMj0iQmFja2dyb3VuZEltYWdlRml4IiByZXN1bHQ9InNoYXBlIi8+CjxmZUdhdXNzaWFuQmx1ciBzdGREZXZpYXRpb249IjUxLjU5MzIiIHJlc3VsdD0iZWZmZWN0MV9mb3JlZ3JvdW5kQmx1cl80MzY4Xzk4MDEiLz4KPC9maWx0ZXI+CjwvZGVmcz4KPC9zdmc+Cg==" alt="">
  <div class="h-auto -z-10 top-10 flex justify-center items-center gap-5 text-white bg-purple-500 rounded-3xl flex-col p-10">
    <!-- <img class="sm:hidden lg:flex mr-auto " src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQyIiBoZWlnaHQ9IjIxNiIgdmlld0JveD0iMCAwIDI0MiAyMTYiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIG9wYWNpdHk9IjAuMyI+CjxwYXRoIGZpbGwtcnVsZT0iZXZlbm9kZCIgY2xpcC1ydWxlPSJldmVub2RkIiBkPSJNMjM5LjI2OCA0NS44NzUxQzIzOS4xMDQgNTEuMTA5IDIzNC43MjcgNTUuMjIwMiAyMjkuNDk0IDU1LjA1NzRDMjI0LjI1OSA1NC44OTMzIDIyMC4xNDggNTAuNTE1NyAyMjAuMzExIDQ1LjI4MThDMjIwLjQ3NSA0MC4wNDY4IDIyNC44NTIgMzUuOTM2NyAyMzAuMDg2IDM2LjEwMDdDMjM1LjMyMSAzNi4yNjM2IDIzOS40MzIgNDAuNjQwMSAyMzkuMjY4IDQ1Ljg3NTFaIiBzdHJva2U9IiNFMEUwRTAiIHN0cm9rZS13aWR0aD0iNCIvPgo8cGF0aCBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTI0LjMyMjcgMjAzLjkyNkMyNC4xNTg1IDIwOS4xNiAxOS43ODIgMjEzLjI3MSAxNC41NDgyIDIxMy4xMDhDOS4zMTMyOSAyMTIuOTQ0IDUuMjAyOTggMjA4LjU2NiA1LjM2NjAyIDIwMy4zMzNDNS41MzAxNiAxOTguMDk4IDkuOTA2NjUgMTkzLjk4NyAxNS4xNDA1IDE5NC4xNTFDMjAuMzc1NCAxOTQuMzE0IDI0LjQ4NjggMTk4LjY5MSAyNC4zMjI3IDIwMy45MjZaIiBzdHJva2U9IiNFMEUwRTAiIHN0cm9rZS13aWR0aD0iNCIvPgo8cGF0aCBkPSJNNzcuMDAyIC0xMC4zMTE3Qzc3LjAwMiAtMTAuMzExNyAxMTkuNjE1IC0xMDMuODU5IDIyMC4zMDEgLTE4Ljc5NjVDMjIwLjMwMSAtMTguNzk2NSAxODMuMzE2IDk4LjAxNzcgOTAuNDQgNDUuODY5OCIgc3Ryb2tlPSIjRTBFMEUwIiBzdHJva2Utd2lkdGg9IjQiLz4KPHBhdGggZD0iTTk4Ljg5NTcgMTcuNjU1M0M5OC44OTU3IDE3LjY1NTMgMjAzLjEwOCAtMTAuMjUwNCAyMTMuOTg5IDExNS42MTRDMjEzLjk4OSAxMTUuNjE0IDk4Ljc3NDIgMTc4LjA5NSA3MC42ODk1IDY2LjM4ODUiIHN0cm9rZT0iI0UwRTBFMCIgc3Ryb2tlLXdpZHRoPSI0Ii8+CjxwYXRoIGQ9Ik04LjgzMTcyIDIuMzc2MDFDOC44MzE3MiAyLjM3NjAxIC03Ny40MTcgLTQyLjMyNzYgMTIuNzgwMSAtMTM2LjcwOUMxMi43ODAxIC0xMzYuNzA5IDEzNy4yMjQgLTEwNi41NiA4MS43MTU0IC0xOS4zMjA4IiBzdHJva2U9IiNFMEUwRTAiIHN0cm9rZS13aWR0aD0iNCIvPgo8cGF0aCBkPSJNNDIuNzMwNCAtMjQuMzI4NkM0Mi43MzA0IC0yNC4zMjg2IDE5LjQ5OTkgLTEyMC44MDQgMTUyLjk4IC0xMzAuMzg1QzE1Mi45OCAtMTMwLjM4NSAyMTYuMDQgLTExLjE4MzIgOTcuNDQ3IDE1LjAyMjMiIHN0cm9rZT0iI0UwRTBFMCIgc3Ryb2tlLXdpZHRoPSI0Ii8+CjxwYXRoIGQ9Ik05MS4wNzAyIDQ2LjYzMTFDOTEuMDcwMiA0Ni42MzExIDE4MS41ODYgOTUuMDU5OCA5Mi43MzggMTg5LjkzMUM5Mi43MzggMTg5LjkzMSAtMzMuNTY3MiAxNjAuMjQxIDI1LjEyOTkgNjQuODUyOCIgc3Ryb2tlPSIjRTBFMEUwIiBzdHJva2Utd2lkdGg9IjQiLz4KPHBhdGggZD0iTTY4LjYyNTkgNjUuNzM3N0M2OC42MjU5IDY1LjczNzcgOTQuNzUzMSAxNTkuMTY0IC0zOC44NzYxIDE2Ni43NTFDLTM4Ljg3NjEgMTY2Ljc1MSAtMTAxLjk1NSA2MS42OSAxLjg2ODc1IDM2LjA5NTkiIHN0cm9rZT0iI0UwRTBFMCIgc3Ryb2tlLXdpZHRoPSI0Ii8+CjxwYXRoIGQ9Ik0yMC4xMDk1IDY0LjM4MjJDMjAuMTA5NSA2NC4zODIyIC0zNC4wODY2IDE1MC42MTcgLTEzNS44MzQgNjcuMTA3OEMtMTM1LjgzNCA2Ny4xMDc4IC05OS42NTY3IC01OS4wNTMyIDMuNzQ4NjEgMi4zODYwNSIgc3Ryb2tlPSIjRTBFMEUwIiBzdHJva2Utd2lkdGg9IjQiLz4KPHBhdGggZD0iTTEuNzQ0NTYgMzMuMjMwNUMxLjc0NDU2IDMzLjIzMDUgLTk3LjA1NDggNjIuNDAwNyAtMTA0LjIyNSAtNjUuNDE4Qy0xMDQuMjI1IC02NS40MTggMTQuMjk0NCAtMTMyLjYxMyA0My4yODk1IC0yNC45NDUzIiBzdHJva2U9IiNFMEUwRTAiIHN0cm9rZS13aWR0aD0iNCIvPgo8cGF0aCBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTg5LjM4OTQgNDcuNTIzOUM3Ni4wODU0IDY5LjA3MTggNDcuMDIgNzYuMjM1NSAyNC40NjkyIDYzLjUyMTdDMS45MTg0IDUwLjgwOSAtNS41Nzc4MSAyMy4wMzU0IDcuNzI2MjQgMS40ODc0OEMyMS4wMzAzIC0yMC4wNjE1IDUwLjA5NTcgLTI3LjIyNDEgNzIuNjQ2NSAtMTQuNTExNEM5NS4xOTczIC0xLjc5ODY1IDEwMi42OTMgMjUuOTc0OSA4OS4zODk0IDQ3LjUyMzlaIiBzdHJva2U9IiNFMEUwRTAiIHN0cm9rZS13aWR0aD0iNCIvPgo8L2c+Cjwvc3ZnPgo=" alt=""> -->
    <h1 class="text-5xl font-extrabold"><span class="line-through text-gray-400 text-lg">2%</span>    Free*</h1>
    <p class=" text-gray-100">Sign up for</p>
    <h1 class="text-2xl font-bold">PhonePe Payment Gateway</h1>
    <p class=" text-gray-200">Zero Transaction Fee. Zero Setup Fee.</p>
    <p class=" text-gray-200">Zero Hidden Charges.</p>
    <button class="bg-white text-black py-2 px-12 rounded-3xl">Get Started</button>
  </div>
</div>

<div class="mb-16">
  <img class="sm:h-14 sm:mb-24 lg:h-20 lg:ml-auto" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzEiIGhlaWdodD0iMzkiIHZpZXdCb3g9IjAgMCAzMSAzOSIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHJlY3Qgb3BhY2l0eT0iMC44ODg2MDEiIHg9Ii02LjY5MzM2IiB5PSIwLjU2MjUiIHdpZHRoPSIzNy4yNjQyIiBoZWlnaHQ9IjM3Ljc2MTEiIHJ4PSI3LjM5MTcyIiBmaWxsPSIjQzlCNUU1Ii8+Cjwvc3ZnPgo=" alt="">
</div>

<div class="flex justify-center text-center sm:flex-col text-2xl sm:font-bold mb-14 lg:text-5xl lg:text-left lg:font-thin px-20 lg:flex-row lg:w-full items-center">
  <div class="lg:flex">Here’s why India’s leading businesses prefer PhonePe Payment Gateway</div>
  <img class="sm:hidden lg:flex" src="https://www.phonepe.com/webstatic/6992/static/a05cb94f9a0e197b2bb489aa2b88099d/bc8e0/why-phonepe-pg.png" alt="">
</div>


<div class="sm:p-5 lg:px-32 grid-cols-2 grid-rows-2 grid gap-5 mb-16">
  <div class=" bg-orange-100 rounded-2xl flex flex-col p-5 gap-5">
    <img class="h-16 mr-auto" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTA4IiBoZWlnaHQ9IjEwOSIgdmlld0JveD0iMCAwIDEwOCAxMDkiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF80MzAxXzYxNDMpIj4KPHJlY3QgeT0iMC42NTYyNSIgd2lkdGg9IjEwOCIgaGVpZ2h0PSIxMDgiIHJ4PSIxMy43OTA3IiBmaWxsPSIjRkRDQzlBIi8+CjxwYXRoIGQ9Ik02Mi40Mjg3IDMwLjE4NjJDNjIuNDI4NyAyOS4wNiA2MS41ODUgMjYuNjU2MiA1OS4wMjE4IDI2LjY1NjJDNTcuNTI4NyAyNi42NTYyIDU2LjE1MjEgMjcuNjU4OSA1NS43MjI3IDI5LjIxOEw0Mi4wNTI0IDc4LjcyOThDNDEuOTYyNiA3OS4wNTQyIDQxLjkxOTggNzkuMzgxIDQxLjkxOTggNzkuNzAyNUM0MS44MjcgODAuODQyOSA0Mi43Nzc1IDgzLjI0MTEgNDUuMzQwNyA4My4yNDExQzQ2LjgyNzQgODMuMjQxMSA0OC4xOTU1IDgyLjIyOTEgNDguNjI0OCA4MC42NzQ5TDYyLjI5NTIgMzEuMTYzMUM2Mi4zODYgMzAuODM0OSA2Mi40Mjg3IDMwLjUwNzggNjIuNDI4NyAzMC4xODYyWk0zNi43OTY4IDQyLjQ3MTNDMzYuNzk2OCA0MC40NTEgMzUuMjAwMSAzOC45MzQ3IDMzLjM3OTIgMzguOTM0N0MzMi41MDQ3IDM4LjkzNDcgMzEuNjI5OCAzOS4yODAxIDMwLjk2MzQgMzkuOTcwOUwxOS4wMDE4IDUyLjM0ODlDMTguMzMzNyA1My4xMzYyIDE4IDU0LjA0MjUgMTggNTQuODQ5MkMxOCA1NS42NTYgMTguMzMzNyA1Ni43NjEyIDE5LjAwMTIgNTcuNDQ2NEwzMC45NjI4IDY5LjgyNDNDMzEuNjI3NiA3MC41MjA2IDMyLjUwMzQgNzAuNzYzNyAzMy4zNzkyIDcwLjc2MzdDMzUuMjAwMSA3MC43NjM3IDM2Ljc5NjggNjkuMjQ2MyAzNi43OTY4IDY3LjIyNzJDMzYuNzk2OCA2Ni4zMjIzIDM2LjQ2MyA2NS40MTY5IDM1Ljc5NTUgNjQuNzI2MkwyNi4yNTAzIDU0Ljg0OTJMMzUuNzk2IDQ0Ljk3MTJDMzYuNDY1NyA0NC4zNzIyIDM2Ljc5NjggNDMuNDc3IDM2Ljc5NjggNDIuNDcxM1pNODYuMzUxOCA1NC44NDkyQzg2LjM1MTggNTMuOTQ0MyA4Ni4wMTgxIDUzLjAzOSA4NS4zNTA2IDUyLjM0ODJMNzMuMzg5IDM5Ljk3MDNDNzIuNzI0MiAzOS4zNzY4IDcxLjg0ODQgMzguOTM0NyA3MC45NzI3IDM4LjkzNDdDNjkuMTUxNyAzOC45MzQ3IDY3LjU1NTEgNDAuNDUyMSA2Ny41NTUxIDQyLjQ3MTNDNjcuNTU1MSA0My4zNzYyIDY3Ljg4ODggNDQuMjgxNiA2OC41NTYzIDQ0Ljk3MjNMNzguMTAyMSA1NC44NTAzTDY4LjU1NjMgNjQuNzI4NEM2Ny44ODYxIDY1LjUxNDIgNjcuNTU1MSA2Ni40MjA0IDY3LjU1NTEgNjcuMjI3MkM2Ny41NTUxIDY5LjI0NzQgNjkuMTUxNyA3MC43NjM3IDcwLjk3MjcgNzAuNzYzN0M3MS44NDcxIDcwLjc2MzcgNzIuNzIyIDcwLjQxODQgNzMuMzg4NSA2OS43Mjc1TDg1LjM1IDU3LjM0OTZDODYuMDIwNyA1Ni43NjEyIDg2LjM1MTggNTUuODU0OSA4Ni4zNTE4IDU0Ljg0OTJaIiBmaWxsPSJ3aGl0ZSIvPgo8L2c+CjxkZWZzPgo8Y2xpcFBhdGggaWQ9ImNsaXAwXzQzMDFfNjE0MyI+CjxyZWN0IHdpZHRoPSIxMDgiIGhlaWdodD0iMTA4IiBmaWxsPSJ3aGl0ZSIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMCAwLjY1NjI1KSIvPgo8L2NsaXBQYXRoPgo8L2RlZnM+Cjwvc3ZnPgo=" alt="">
    <h1 class="text-xl font-bold">Effortless Integration</h1>
    <p>Our developer-friendly APIs, plugins & libraries for all major languages & platforms make integration easy, allowing you to focus on growing your business.</p>
  </div>  
  <div class=" bg-violet-100 rounded-2xl flex flex-col p-5 gap-5">
    <img class="h-16 mr-auto" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTA4IiBoZWlnaHQ9IjEwOSIgdmlld0JveD0iMCAwIDEwOCAxMDkiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF80MzAxXzYxNDQpIj4KPHJlY3QgeT0iMC42NTYyNSIgd2lkdGg9IjEwOCIgaGVpZ2h0PSIxMDgiIHJ4PSIxMy43OTA3IiBmaWxsPSIjRTBEMEZFIi8+CjxyZWN0IHg9IjMyIiB5PSI1My42Mjg5IiB3aWR0aD0iMTMuNTUzMiIgaGVpZ2h0PSIyMS42ODUxIiBzdHJva2U9IiM3MDU1QzIiIHN0cm9rZS13aWR0aD0iNS4wMTIzNiIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8cmVjdCB4PSI0NS41NTQ3IiB5PSI0My42OTUzIiB3aWR0aD0iMTMuNTUzMiIgaGVpZ2h0PSIzMS42MjQxIiBzdHJva2U9IiM3MDU1QzIiIHN0cm9rZS13aWR0aD0iNS4wMTIzNiIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8cmVjdCB4PSI1OS4xMDk0IiB5PSIzNC42NTYyIiB3aWR0aD0iMTMuNTUzMiIgaGVpZ2h0PSI0MC42NTk1IiBzdHJva2U9IiM3MDU1QzIiIHN0cm9rZS13aWR0aD0iNS4wMTIzNiIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L2c+CjxkZWZzPgo8Y2xpcFBhdGggaWQ9ImNsaXAwXzQzMDFfNjE0NCI+CjxyZWN0IHdpZHRoPSIxMDgiIGhlaWdodD0iMTA4IiBmaWxsPSJ3aGl0ZSIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMCAwLjY1NjI1KSIvPgo8L2NsaXBQYXRoPgo8L2RlZnM+Cjwvc3ZnPgo=" alt="">
    <h1 class="text-xl font-bold">Industry-Best Success Rates</h1>
    <p>Our developer-friendly APIs, plugins & libraries for all major languages & platforms make integration easy, allowing you to focus on growing your business.</p>
  </div>
  <div class=" bg-violet-100 rounded-2xl flex flex-col p-5 gap-5">
    <img class="h-16 mr-auto" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTA4IiBoZWlnaHQ9IjEwOSIgdmlld0JveD0iMCAwIDEwOCAxMDkiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF80MzAxXzYxNDUpIj4KPHJlY3QgeT0iMC42NTYyNSIgd2lkdGg9IjEwOCIgaGVpZ2h0PSIxMDgiIHJ4PSIxMy43OTA3IiBmaWxsPSIjRTBEMEZFIi8+CjxwYXRoIGQ9Ik01NC4wNjY3IDgyLjU5OTRDNTQuMDY2NyA4Mi41OTk0IDc0Ljg5NzEgNzIuMTg0MiA3NC44OTcxIDU2LjU2MTRWMzguMzM0OEw1NC4wNjY3IDMwLjUyMzRMMzMuMjM2MyAzOC4zMzQ4VjU2LjU2MTRDMzMuMjM2MyA3Mi4xODQyIDU0LjA2NjcgODIuNTk5NCA1NC4wNjY3IDgyLjU5OTRaIiBzdHJva2U9IiM3MDU1QzIiIHN0cm9rZS13aWR0aD0iNS4yMDc2IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPHBhdGggZD0iTTQ2LjI1NTkgNTYuNTYzMUw1MS40NjM1IDYxLjc3MDdMNjEuODc4NyA1MS4zNTU1IiBzdHJva2U9IiM3MDU1QzIiIHN0cm9rZS13aWR0aD0iNS4yMDc2IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9nPgo8ZGVmcz4KPGNsaXBQYXRoIGlkPSJjbGlwMF80MzAxXzYxNDUiPgo8cmVjdCB3aWR0aD0iMTA4IiBoZWlnaHQ9IjEwOCIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAgMC42NTYyNSkiLz4KPC9jbGlwUGF0aD4KPC9kZWZzPgo8L3N2Zz4K" alt="">
    <h1 class="text-xl font-bold">Secure & Compliant</h1>
    <p>Our developer-friendly APIs, plugins & libraries for all major languages & platforms make integration easy, allowing you to focus on growing your business.</p>
  </div>
  <div class=" bg-orange-100 rounded-2xl flex flex-col p-5 gap-5">
    <img class="h-16 mr-auto" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTA4IiBoZWlnaHQ9IjEwOSIgdmlld0JveD0iMCAwIDEwOCAxMDkiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF80MzAxXzYxNDYpIj4KPHJlY3QgeT0iMC42NTYyNSIgd2lkdGg9IjEwOCIgaGVpZ2h0PSIxMDgiIHJ4PSIxMy43OTA3IiBmaWxsPSIjRjZDMjhFIi8+CjxjaXJjbGUgY3g9IjUzLjk5NDciIGN5PSI1NC42NTQ5IiByPSIzMC4yOTk0IiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjUuNDkxNTMiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik02MS4wNTA0IDQzLjQ3ODhWNDcuMTE5M0g2NS40OTE2VjUwLjU0NzVINjAuOTE5OEM2MC41NzE3IDUzLjA4NzUgNTkuNDc1NiA1NS4wMDcxIDU3LjYzMiA1Ni4zMDQzQzU1Ljc4ODUgNTcuNjAyOCA1Mi45Nzk0IDU4LjI1MTQgNDkuMjA2MSA1OC4yNTE0VjYwLjkxODJDNDkuMjA2MSA2My44NTM3IDUwLjQ1NDIgNjUuMzIwNyA1Mi45NTExIDY1LjMyMDdDNTQuMTcwMiA2NS4zMjA3IDU1LjA3NzEgNjQuOTU0MSA1NS42NzI1IDY0LjIxOTZDNTYuMjY3MiA2My40ODY0IDU2LjU2NTYgNjIuMzg2IDU2LjU2NTYgNjAuOTE4Mkg2Mi4yNjk1QzYyLjE1MzQgNjMuNzEyIDYxLjMyNiA2NS44OTIxIDU5Ljc4NzggNjcuNDU3OUM1OC4yNDg5IDY5LjAyNDMgNTYuMDU3MiA2OS44MDcxIDUzLjIxMjIgNjkuODA3MUM1MC4wNDgxIDY5LjgwNzEgNDcuNjMxMyA2OC45OTYxIDQ1Ljk2MTggNjcuMzczM0M0NC4yOTI0IDY1Ljc1MTEgNDMuNDU4IDYzLjMxNzIgNDMuNDU4IDYwLjA3MTZWNTQuMzU3MUM0Ni42MjIyIDU0LjM1NzEgNDguOTg4NSA1NC4yNjU4IDUwLjU1NTcgNTQuMDgxOUM1Mi4xMjM2IDUzLjg5OTIgNTMuMjQ4MSA1My41Mzk0IDUzLjkzMDUgNTMuMDAyOUM1NC42MTIzIDUyLjQ2NzEgNTUuMDQxMiA1MS42NDggNTUuMjE1MyA1MC41NDc1SDQyLjVWNDcuMTE5M0g1NS4zMDIzVjQzLjQ3ODhINDIuNVYzOS41SDY1LjQ5MTZWNDMuNDc4OEg2MS4wNTA0WiIgZmlsbD0id2hpdGUiLz4KPC9nPgo8ZGVmcz4KPGNsaXBQYXRoIGlkPSJjbGlwMF80MzAxXzYxNDYiPgo8cmVjdCB3aWR0aD0iMTA4IiBoZWlnaHQ9IjEwOCIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAgMC42NTYyNSkiLz4KPC9jbGlwUGF0aD4KPC9kZWZzPgo8L3N2Zz4K" alt="">
    <h1 class="text-xl font-bold">Multiple Payment Methods</h1>
    <p>Our developer-friendly APIs, plugins & libraries for all major languages & platforms make integration easy, allowing you to focus on growing your business.</p>
  </div>
</div>


<div class="flex justify-center text-center flex-col gap-3 mb-16">
  <img class="sm:h-16 lg:h-24" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTExIiBoZWlnaHQ9IjEwOSIgdmlld0JveD0iMCAwIDExMSAxMDkiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHg9IjAuODcxMDk0IiB5PSIwLjA1MDc4MTIiIHdpZHRoPSIxMDkuNjc0IiBoZWlnaHQ9IjEwOCIgcng9IjIxLjc2NzQiIGZpbGw9InVybCgjcGFpbnQwX2xpbmVhcl80MzEwXzUwMDApIi8+CjxyZWN0IHg9IjIwLjk5NjEiIHk9IjUxLjcwMzEiIHdpZHRoPSIxMC4zNDE5IiBoZWlnaHQ9IjMyLjkwNjIiIHJ4PSI1LjE3MDk3IiBmaWxsPSJ3aGl0ZSIvPgo8cmVjdCB4PSI1MS43MTQ4IiB5PSI0NC40OTIyIiB3aWR0aD0iMTAuMzQxOSIgaGVpZ2h0PSI0MC4xMTQyIiByeD0iNS4xNzA5NyIgZmlsbD0id2hpdGUiLz4KPHJlY3QgeD0iNjYuNzQ2MSIgeT0iMjYuMDAzOSIgd2lkdGg9IjEwLjM0MTkiIGhlaWdodD0iNTguNjA0MyIgcng9IjUuMTcwOTciIGZpbGw9IndoaXRlIi8+CjxyZWN0IHg9IjM2LjY2OCIgeT0iNTguOTEwMiIgd2lkdGg9IjEwLjM0MTkiIGhlaWdodD0iMjUuNjk4MSIgcng9IjUuMTcwOTciIGZpbGw9IndoaXRlIi8+CjxyZWN0IHg9IjgwLjU3NDIiIHk9IjU4LjkxMDIiIHdpZHRoPSIxMC4zNDE5IiBoZWlnaHQ9IjI1LjY5ODEiIHJ4PSI1LjE3MDk3IiBmaWxsPSJ3aGl0ZSIvPgo8ZGVmcz4KPGxpbmVhckdyYWRpZW50IGlkPSJwYWludDBfbGluZWFyXzQzMTBfNTAwMCIgeDE9IjM2LjAzMzkiIHkxPSIwLjA1MDc4MSIgeDI9IjU1LjcwODMiIHkyPSIxMDguMDUxIiBncmFkaWVudFVuaXRzPSJ1c2VyU3BhY2VPblVzZSI+CjxzdG9wIHN0b3AtY29sb3I9IiM1NkU5RkYiLz4KPHN0b3Agb2Zmc2V0PSIxIiBzdG9wLWNvbG9yPSIjOUE3NUNBIi8+CjwvbGluZWFyR3JhZGllbnQ+CjwvZGVmcz4KPC9zdmc+Cg==" alt="">
  <h1 class="sm:text-2xl lg:text-4xl font-bold">Powerful Centralised Dashboard</h1>
  <p class="lg:text-xl">Access comprehensive reports and statistics for key metrics, gaining insights for informed business decisions</p>
</div>

<div>
  <img class="flex justify-center mx-auto" src="https://www.phonepe.com/webstatic/6992/static/3d94bd6c69f5fa29b3b17c908f4dde71/d96a9/pg-dashboard-mobile.png" alt="">
</div>
<div class="flex sm:p-3 sm:items-center sm:justify-center sm:w-svw mt-5">
      <div class="bg-purple-700 rounded-3xl items-center justify-center p-3 px-9 text-white">GET STARTED FOR FREE</div>    
</div>

<div class="flex justify-center sm:my-5 lg:my-20 font-bold sm:text-2xl lg:text-4xl">
  <h1>Trusted by India’s largest online brands</h1>
</div>

<div>
  <div class="p-5 rounded-2xl flex justify-center">
    <img class="" src="https://www.phonepe.com/webstatic/6992/static/30208cfb7b89e80008ee5e036b78ad67/c81c9/dream-11-bg-mweb.webp" alt="">
    <div class="flex ">
      <!-- <p class=" bottom-56 pl-8 pr-8 text-justify text-white absolute"> ipsum dolor sit amet consectetur adipisicing elitlit ad quam magnam odit officia. Nam, placeat sit in explicabo at ut voluptate quidem suscipit neque accusantium blanditiis amet. Fuga deserunt, aspernatur incidunt rem sed laborum consequatur molestiae dolores voluptates. Explicabo consectetur incidunt nesciunt nulla.</p> -->
      <!-- <h1 class=" bottom-48 pl-8 pr-8 text-justify text-white absolute font-bold">Vaibhav Kokal</h1>
      <p class=" bottom-40 pl-8 pr-8 text-justify text-white absolute">CEO</p> -->
      <!-- <img class=" bottom-32 pl-8 pr-8 text-justify text-white absolute h-6" src="https://www.phonepe.com/webstatic/6992/static/05c4544c484a4131779cc898ce9f037b/16eb0/dream-11-bw.webp" alt=""> -->
      <div class="flex">
      <!-- <div class="flex">
        <h1 class="z-10 bottom-20 text-white text-2xl pl-8 pr-8 text-justify absolute">1900+</h1>
        <p class="z-10 bottom-5 text-white  pl-8 pr-8 text-sm text-justify absolute">TPS During Peak <br> IPL week</p>
      </div> -->
      <!-- <div class="flex">
        <h1 class="z-10 bottom-20 text-white text-2xl pl-8 pr-8 text-justify absolute">Why PhonePe PG?</h1>
        <p class="z-10 bottom-5 text-white  pl-8 pr-8 text-sm text-justify absolute"><ul class="z-10 bottom-5 text-white  pl-8 pr-8 text-sm text-justify absolute"><li>Consistent support during IPL</li> <li>Responsive support</li></ul></p>
      </div> -->
    </div>
    </div>
  </div>
</div>

<div class="flex sm:p-3 sm:items-center sm:justify-center sm:w-svw my-5">
      <div class="bg-purple-700 rounded-3xl items-center justify-center p-3 px-9 text-white">GET STARTED FOR FREE</div>    
</div>


<div class="flex justify-center flex-col text-center">
  <img class="h-16 mt-20" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTEyIiBoZWlnaHQ9IjExMCIgdmlld0JveD0iMCAwIDExMiAxMTAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF80NzY1XzEyMzIpIj4KPHBhdGggZD0iTS0wLjI1MzkwNiAyMi4yNzkzQy0wLjI1MzkwNiAxMC4wMDI2IDkuNjk4MzYgMC4wNTAyOTMgMjEuOTc1MSAwLjA1MDI5M0g4OS41MTcxQzEwMS43OTQgMC4wNTAyOTMgMTExLjc0NiAxMC4wMDI2IDExMS43NDYgMjIuMjc5M1Y4OC4xMTE0QzExMS43NDYgMTAwLjM4OCAxMDEuNzk0IDExMC4zNCA4OS41MTcxIDExMC4zNEgyMS45NzUxQzkuNjk4MzYgMTEwLjM0IC0wLjI1MzkwNiAxMDAuMzg4IC0wLjI1MzkwNiA4OC4xMTE0VjIyLjI3OTNaIiBmaWxsPSJ1cmwoI3BhaW50MF9saW5lYXJfNDc2NV8xMjMyKSIvPgo8cmVjdCB4PSI1Mi43NTM5IiB5PSI1OS4wNDI1IiB3aWR0aD0iMzUuOTA4NCIgaGVpZ2h0PSIyNi41MDM4IiBmaWxsPSJ3aGl0ZSIvPgo8cGF0aCBkPSJNODcuNzYxNSAxNC4wODk4Qzg5LjM0NDUgMTYuODMxNyA5MC4zNzE5IDE5Ljg1ODUgOTAuNzg1MiAyMi45OTc0QzkxLjE5ODQgMjYuMTM2NCA5MC45ODk0IDI5LjMyNiA5MC4xNyAzMi4zODQxQzg5LjM1MDUgMzUuNDQyMyA4Ny45MzY4IDM4LjMwOTEgODYuMDA5NCA0MC44MjA4Qzg0LjA4MjEgNDMuMzMyNiA4MS42Nzg5IDQ1LjQ0MDIgNzguOTM3IDQ3LjAyMzJDNzYuMTk1MiA0OC42MDYyIDczLjE2ODMgNDkuNjMzNyA3MC4wMjk0IDUwLjA0NjlDNjYuODkwNSA1MC40NjAyIDYzLjcwMDkgNTAuMjUxMSA2MC42NDI3IDQ5LjQzMTdDNTcuNTg0NiA0OC42MTIzIDU0LjcxNzggNDcuMTk4NSA1Mi4yMDYgNDUuMjcxMkM0OS42OTQyIDQzLjM0MzggNDcuNTg2NyA0MC45NDA2IDQ2LjAwMzcgMzguMTk4N0w2Ni44ODI2IDI2LjE0NDNMODcuNzYxNSAxNC4wODk4WiIgZmlsbD0iI0ZGREU5RiIvPgo8Y2lyY2xlIGN4PSIyOC4zOTEiIGN5PSI2OS43MzA0IiByPSIxNS44MTY4IiBmaWxsPSJ3aGl0ZSIvPgo8L2c+CjxkZWZzPgo8bGluZWFyR3JhZGllbnQgaWQ9InBhaW50MF9saW5lYXJfNDc2NV8xMjMyIiB4MT0iNTUuNzQ2MSIgeTE9IjAuMDUwMjkzIiB4Mj0iNTUuNzQ2MSIgeTI9IjExMC4zNCIgZ3JhZGllbnRVbml0cz0idXNlclNwYWNlT25Vc2UiPgo8c3RvcCBzdG9wLWNvbG9yPSIjNjcyQkQxIi8+CjxzdG9wIG9mZnNldD0iMSIgc3RvcC1jb2xvcj0iI0VDODk2QyIvPgo8L2xpbmVhckdyYWRpZW50Pgo8Y2xpcFBhdGggaWQ9ImNsaXAwXzQ3NjVfMTIzMiI+CjxyZWN0IHdpZHRoPSIxMTIiIGhlaWdodD0iMTEwIiBmaWxsPSJ3aGl0ZSIvPgo8L2NsaXBQYXRoPgo8L2RlZnM+Cjwvc3ZnPgo=" alt="">
  <h1 class="my-5 font-bold text-2xl">Comprehensive Solutions</h1>
  <p class="mb-5">To keep your business ahead of the rest</p>
</div>

<div class="lg:grid lg:grid-cols-3">
  
<div class="pl-5 pr-5 pb-5 flex flex-col justify-center bg-yellow-300 m-5 rounded-2xl">
  <div class="ml-auto">
    <img class="h-48 z-20" src="https://www.phonepe.com/webstatic/6992/static/593dfee534dbf4bdd2b4602ae9bd9849/a6261/pg_solutions_card_qc_1.png" alt="">  
  </div>

  <h1 class="font-bold">Quick Checkout</h1>
  <p class=" text-sm font-thin">Enable customers to complete transactions without exiting your website or application with our unique half-pay-page experience within your checkout.</p>
</div>


<div class=" bg-gray-200 flex p-5 items-center rounded-2xl m-5 gap-7">
  <img class="h-16" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTU0IiBoZWlnaHQ9IjE2MSIgdmlld0JveD0iMCAwIDE1NCAxNjEiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF80MzE1Xzg3MTUpIj4KPGNpcmNsZSBjeD0iNzAuMjg2NiIgY3k9IjcwLjc3MTkiIHI9IjY5Ljk2MDQiIGZpbGw9IiNGNENDN0MiLz4KPGNpcmNsZSBjeD0iNjkuNTc2MiIgY3k9IjcwLjA0ODgiIHI9IjQ3LjgzMDEiIGZpbGw9IiNGRkRFOUYiLz4KPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik03OS45MjkyIDU0Ljc4MlY1OS43NTU1SDg1Ljk5NjdWNjQuNDM5MUg3OS43NTA4Qzc5LjI3NTIgNjcuOTA5MiA3Ny43Nzc3IDcwLjUzMTcgNzUuMjU5MSA3Mi4zMDM5QzcyLjc0MDUgNzQuMDc3OSA2OC45MDI4IDc0Ljk2NCA2My43NDc3IDc0Ljk2NFY3OC42MDc1QzYzLjc0NzcgODIuNjE3OCA2NS40NTI4IDg0LjYyMjEgNjguODY0MSA4NC42MjIxQzcwLjUyOTYgODQuNjIyMSA3MS43Njg2IDg0LjEyMTIgNzIuNTgyIDgzLjExNzdDNzMuMzk0NSA4Mi4xMTYxIDczLjgwMjEgODAuNjEyNiA3My44MDIxIDc4LjYwNzVIODEuNTk0N0M4MS40MzYxIDgyLjQyNDMgODAuMzA1NyA4NS40MDI3IDc4LjIwNDIgODcuNTQxOEM3Ni4xMDE4IDg5LjY4MTggNzMuMTA3NiA5MC43NTEzIDY5LjIyMDggOTAuNzUxM0M2NC44OTggOTAuNzUxMyA2MS41OTYyIDg5LjY0MzMgNTkuMzE1NCA4Ny40MjYyQzU3LjAzNDcgODUuMjEgNTUuODk0OCA4MS44ODQ5IDU1Ljg5NDggNzcuNDUwOFY2OS42NDM4QzYwLjIxNzYgNjkuNjQzOCA2My40NTA0IDY5LjUxOSA2NS41OTE2IDY5LjI2NzdDNjcuNzMzNiA2OS4wMTgyIDY5LjI2OTkgNjguNTI2NSA3MC4yMDIyIDY3Ljc5MzZDNzEuMTMzNSA2Ny4wNjE2IDcxLjcxOTUgNjUuOTQyNiA3MS45NTczIDY0LjQzOTFINTQuNTg1OVY1OS43NTU1SDcyLjA3NjJWNTQuNzgySDU0LjU4NTlWNDkuMzQ2Mkg4NS45OTY3VjU0Ljc4Mkg3OS45MjkyWiIgZmlsbD0iIzJDMTY0NSIvPgo8Y2lyY2xlIGN4PSIxMTQuNjYxIiBjeT0iMTIxLjkwOCIgcj0iMzYuNzQ4OSIgZmlsbD0iIzg5NUFFOCIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIzLjQ1NzQ4Ii8+CjxwYXRoIGQ9Ik0xMTEuNzMgMTIzLjM3M0MxMTIuMzYgMTI0LjIxNSAxMTMuMTYzIDEyNC45MTEgMTE0LjA4NSAxMjUuNDE1QzExNS4wMDcgMTI1LjkxOSAxMTYuMDI3IDEyNi4yMTkgMTE3LjA3NiAxMjYuMjk0QzExOC4xMjQgMTI2LjM2OSAxMTkuMTc2IDEyNi4yMTcgMTIwLjE2IDEyNS44NUMxMjEuMTQ1IDEyNS40ODMgMTIyLjAzOSAxMjQuOTA4IDEyMi43ODIgMTI0LjE2NUwxMjcuMTc5IDExOS43NjhDMTI4LjUxNCAxMTguMzg1IDEyOS4yNTMgMTE2LjUzNCAxMjkuMjM2IDExNC42MTNDMTI5LjIyIDExMi42OTEgMTI4LjQ0OSAxMTAuODUzIDEyNy4wOSAxMDkuNDk0QzEyNS43MzEgMTA4LjEzNSAxMjMuODkzIDEwNy4zNjUgMTIxLjk3MiAxMDcuMzQ4QzEyMC4wNSAxMDcuMzMxIDExOC4xOTkgMTA4LjA3IDExNi44MTcgMTA5LjQwNUwxMTQuMjk2IDExMS45MTEiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMi45MzE0OCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xMTcuNTkyIDEyMC40NTRDMTE2Ljk2MyAxMTkuNjEyIDExNi4xNiAxMTguOTE2IDExNS4yMzcgMTE4LjQxMkMxMTQuMzE1IDExNy45MDggMTEzLjI5NSAxMTcuNjA4IDExMi4yNDcgMTE3LjUzM0MxMTEuMTk5IDExNy40NTggMTEwLjE0NyAxMTcuNjEgMTA5LjE2MiAxMTcuOTc3QzEwOC4xNzcgMTE4LjM0NCAxMDcuMjgzIDExOC45MTkgMTA2LjU0IDExOS42NjJMMTAyLjE0MyAxMjQuMDU5QzEwMC44MDggMTI1LjQ0MiAxMDAuMDcgMTI3LjI5MyAxMDAuMDg2IDEyOS4yMTRDMTAwLjEwMyAxMzEuMTM2IDEwMC44NzQgMTMyLjk3NCAxMDIuMjMyIDEzNC4zMzNDMTAzLjU5MSAxMzUuNjkyIDEwNS40MjkgMTM2LjQ2MiAxMDcuMzUxIDEzNi40NzlDMTA5LjI3MyAxMzYuNDk2IDExMS4xMjQgMTM1Ljc1NyAxMTIuNTA2IDEzNC40MjJMMTE1LjAxMiAxMzEuOTE2IiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjIuOTMxNDgiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L2c+CjxkZWZzPgo8Y2xpcFBhdGggaWQ9ImNsaXAwXzQzMTVfODcxNSI+CjxyZWN0IHdpZHRoPSIxNTIuODEzIiBoZWlnaHQ9IjE1OS41NzQiIGZpbGw9IndoaXRlIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjMyNjE3MiAwLjgxMTUyMykiLz4KPC9jbGlwUGF0aD4KPC9kZWZzPgo8L3N2Zz4K" alt="">
  <div>
    <h1 class="font-bold">Payment Links</h1>
    <p class="text-sm">Collect payments easily through Links</p>
  </div>
</div>



<div class=" bg-gray-200 flex p-5 items-center rounded-2xl m-5 gap-7">
  <img class="h-16" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTg2IiBoZWlnaHQ9IjI3OCIgdmlld0JveD0iMCAwIDE4NiAyNzgiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIG9wYWNpdHk9IjAuMyI+CjxjaXJjbGUgY3g9IjE3OC44NzYiIGN5PSI2LjEyMjAxIiByPSI1LjMzMjk1IiB0cmFuc2Zvcm09InJvdGF0ZSg5MCAxNzguODc2IDYuMTIyMDEpIiBmaWxsPSIjOTg5ODk4Ii8+CjxjaXJjbGUgY3g9IjE3OC44NzYiIGN5PSIzOC4xMjIiIHI9IjUuMzMyOTUiIHRyYW5zZm9ybT0icm90YXRlKDkwIDE3OC44NzYgMzguMTIyKSIgZmlsbD0iIzk4OTg5OCIvPgo8Y2lyY2xlIGN4PSIxNzguODc2IiBjeT0iNzEuMTg0NSIgcj0iNS4zMzI5NSIgdHJhbnNmb3JtPSJyb3RhdGUoOTAgMTc4Ljg3NiA3MS4xODQ1KSIgZmlsbD0iIzk4OTg5OCIvPgo8Y2lyY2xlIGN4PSIxNzguODc2IiBjeT0iMTA0LjI0NyIgcj0iNS4zMzI5NSIgdHJhbnNmb3JtPSJyb3RhdGUoOTAgMTc4Ljg3NiAxMDQuMjQ3KSIgZmlsbD0iIzk4OTg5OCIvPgo8Y2lyY2xlIGN4PSIxNTUuNDA3IiBjeT0iNi4xMjIwMSIgcj0iNS4zMzI5NSIgdHJhbnNmb3JtPSJyb3RhdGUoOTAgMTU1LjQwNyA2LjEyMjAxKSIgZmlsbD0iIzk4OTg5OCIvPgo8Y2lyY2xlIGN4PSIxNTUuNDA3IiBjeT0iMzguMTIyIiByPSI1LjMzMjk1IiB0cmFuc2Zvcm09InJvdGF0ZSg5MCAxNTUuNDA3IDM4LjEyMikiIGZpbGw9IiM5ODk4OTgiLz4KPGNpcmNsZSBjeD0iMTU1LjQwNyIgY3k9IjcxLjE4NDUiIHI9IjUuMzMyOTUiIHRyYW5zZm9ybT0icm90YXRlKDkwIDE1NS40MDcgNzEuMTg0NSkiIGZpbGw9IiM5ODk4OTgiLz4KPGNpcmNsZSBjeD0iMTU1LjQwNyIgY3k9IjEwNC4yNDciIHI9IjUuMzMyOTUiIHRyYW5zZm9ybT0icm90YXRlKDkwIDE1NS40MDcgMTA0LjI0NykiIGZpbGw9IiM5ODk4OTgiLz4KPGNpcmNsZSBjeD0iMTMwLjg3NiIgY3k9IjYuMTIyMDEiIHI9IjUuMzMyOTUiIHRyYW5zZm9ybT0icm90YXRlKDkwIDEzMC44NzYgNi4xMjIwMSkiIGZpbGw9IiM5ODk4OTgiLz4KPGNpcmNsZSBjeD0iMTMwLjg3NiIgY3k9IjM4LjExODEiIHI9IjUuMzMyOTUiIHRyYW5zZm9ybT0icm90YXRlKDkwIDEzMC44NzYgMzguMTE4MSkiIGZpbGw9IiM5ODk4OTgiLz4KPGNpcmNsZSBjeD0iMTMwLjg4NCIgY3k9IjcxLjE4NDUiIHI9IjUuMzMyOTUiIHRyYW5zZm9ybT0icm90YXRlKDkwIDEzMC44ODQgNzEuMTg0NSkiIGZpbGw9IiM5ODk4OTgiLz4KPGNpcmNsZSBjeD0iMTMwLjg3NiIgY3k9IjEwNC4yNDciIHI9IjUuMzMyOTUiIHRyYW5zZm9ybT0icm90YXRlKDkwIDEzMC44NzYgMTA0LjI0NykiIGZpbGw9IiM5ODk4OTgiLz4KPGNpcmNsZSBjeD0iMTA3LjQxNSIgY3k9IjYuMTIyMDEiIHI9IjUuMzMyOTUiIHRyYW5zZm9ybT0icm90YXRlKDkwIDEwNy40MTUgNi4xMjIwMSkiIGZpbGw9IiM5ODk4OTgiLz4KPGNpcmNsZSBjeD0iMTA3LjQxNSIgY3k9IjM4LjEyMiIgcj0iNS4zMzI5NSIgdHJhbnNmb3JtPSJyb3RhdGUoOTAgMTA3LjQxNSAzOC4xMjIpIiBmaWxsPSIjOTg5ODk4Ii8+CjxjaXJjbGUgY3g9IjEwNy40MTUiIGN5PSI3MS4xODQ1IiByPSI1LjMzMjk1IiB0cmFuc2Zvcm09InJvdGF0ZSg5MCAxMDcuNDE1IDcxLjE4NDUpIiBmaWxsPSIjOTg5ODk4Ii8+CjxjaXJjbGUgY3g9IjEwNy40MTUiIGN5PSIxMDQuMjQ3IiByPSI1LjMzMjk1IiB0cmFuc2Zvcm09InJvdGF0ZSg5MCAxMDcuNDE1IDEwNC4yNDcpIiBmaWxsPSIjOTg5ODk4Ii8+CjwvZz4KPHJlY3Qgd2lkdGg9IjExMS40MzEiIGhlaWdodD0iODYuODczMiIgcng9IjE4IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NjAyNSAtMC41IDAuODY2MDI1IDAuNSA3LjU4Mzk4IDIzNC41MDQpIiBmaWxsPSIjODU3MDYyIiBzdHlsZT0ibWl4LWJsZW5kLW1vZGU6bXVsdGlwbHkiLz4KPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik03Mi4wNDkyIDExMS43ODlDNjguNjc3NyAxMTEuNzg5IDY1LjM2NTUgMTEyLjY3NiA2Mi40NDUgMTE0LjM2TDYyLjQzNjUgMTE0LjM2NUw5LjcxMjcyIDE0NC40OTNMOS42OTY2NyAxNDQuNTAyQzYuNzc2OTQgMTQ2LjE4OCA0LjM1MTgzIDE0OC42MTEgMi42NjQ2MiAxNTEuNTNDMC45Nzc0MTQgMTU0LjQ0OSAwLjA4NzQ0MjMgMTU3Ljc2IDAuMDgzOTg0NCAxNjEuMTMyVjIyMS40MTRDMC4wODc0NDIzIDIyNC43ODYgMC45Nzc0MTUgMjI4LjA5NyAyLjY2NDYyIDIzMS4wMTZDNC4zNTE4MyAyMzMuOTM1IDYuNzc2OTQgMjM2LjM1OSA5LjY5NjY3IDIzOC4wNDRMOS43MTI3MiAyMzguMDU0TDYyLjQzNjUgMjY4LjE4MUw2Mi40NDU3IDI2OC4xODdDNjUuMTk5MiAyNjkuNzc1IDY4LjMwMDggMjcwLjY1MyA3MS40NzIxIDI3MC43NDlDNzEuNjYyNCAyNzAuNzc1IDcxLjg1NjkgMjcwLjc4OSA3Mi4wNTQ2IDI3MC43ODlDNzIuMjUzMyAyNzAuNzg5IDcyLjQ0ODcgMjcwLjc3NSA3Mi42NCAyNzAuNzQ4Qzc1LjgxIDI3MC42NTEgNzguOTEgMjY5Ljc3IDgxLjY2MTkgMjY4LjE4MUw4MS43MDU2IDI2OC4xNTZMODEuNzA4MSAyNjguMTU0TDgxLjcxNTUgMjY4LjE1TDg0LjA1MzcgMjY2Ljc2MkM4NS41NTIyIDI2NS44NzMgODcuNjk5NiAyNjQuNTk4IDkwLjI5NDggMjYzLjA1OUM5NS40ODU0IDI1OS45NzkgMTAyLjQ2NyAyNTUuODM4IDEwOS42MzMgMjUxLjU5M0MxMjMuOTkyIDI0My4wODUgMTM5LjAxNCAyMzQuMjAyIDE0MS45MTYgMjMyLjU0N0MxNDMuMjEzIDIzMS44MDggMTQ0LjAxNCAyMzAuNDI5IDE0NC4wMTQgMjI4LjkzNlYxNjEuMTMyQzE0NC4wMTEgMTU3Ljc2IDE0My4xMjEgMTU0LjQ0OSAxNDEuNDM0IDE1MS41M0MxMzkuNzQ3IDE0OC42MTEgMTM3LjMyMiAxNDYuMTg4IDEzNC40MDIgMTQ0LjUwMkw4MS42NjE5IDExNC4zNjVMODEuNjUzNSAxMTQuMzZDNzguNzMyOSAxMTIuNjc2IDc1LjQyMDcgMTExLjc4OSA3Mi4wNDkyIDExMS43ODlaIiBmaWxsPSIjRUM4OTZDIi8+CjxwYXRoIGQ9Ik00Mi43Njc4IDE3OS4wOTdDNDIuODA3NCAxNzkuMTIgNDIuODU2NyAxNzkuMTE4IDQyLjg5NDkgMTc5LjA5M0wxMTMuNDk0IDEzMi4zNjZMOTcuOTIzMSAxMjMuNDE0TDI3LjA5MDIgMTY5LjY5OUMyNy4wNjU1IDE2OS43MTUgMjcuMDM0NiAxNjkuNzE4IDI3LjAwNjkgMTY5LjcwOEMyNi45NDYzIDE2OS42ODUgMjYuODgxNiAxNjkuNzMgMjYuODgxNiAxNjkuNzk1TDI2Ljg4MDkgMjExLjExMUwzNC40MDM1IDIwNy43MzdMNDIuNTg2OCAyMTguNTg1VjE3OS4yMDFDNDIuNTg2OCAxNzkuMTA4IDQyLjY4NzUgMTc5LjA1IDQyLjc2NzggMTc5LjA5N1oiIGZpbGw9IiNGREVEQjkiLz4KPGNpcmNsZSBjeD0iMTU0LjU4NCIgY3k9IjE1OC4yODkiIHI9IjI5IiBmaWxsPSIjMUZCQ0QzIiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjMiLz4KPHBhdGggZD0iTTE0Mi41ODQgMTU5LjI4OUwxNDkuMDg0IDE2NS43ODlMMTY4LjA4NCAxNDYuNzg5IiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIvPgo8L3N2Zz4K" alt="">
  <div>
    <h1 class="font-bold">Payment Links</h1>
    <p class="text-sm">Collect payments easily through Links</p>
  </div>
</div>


<div class=" bg-gray-200 flex p-5 items-center rounded-2xl m-5 gap-7">
  <img class="h-16" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjU2IiBoZWlnaHQ9IjI1NiIgdmlld0JveD0iMCAwIDI1NiAyNTYiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF80MzE5XzkyNDMpIj4KPGNpcmNsZSBjeD0iMTI2LjMwMSIgY3k9IjEyNy45NTciIHI9IjcxLjU3NjQiIGZpbGw9IiMzNjE5NjgiIHN0cm9rZT0iIzlBNzVDQSIgc3Ryb2tlLXdpZHRoPSI3LjcxMDI5Ii8+CjxwYXRoIGQ9Ik0xMDguNjI1IDk1LjcwOUg5Ny43MTY0Qzk1LjcwODEgOTUuNzA5IDk0LjA4MDEgOTcuMzM3IDk0LjA4MDEgOTkuMzQ1M1YxMTAuMjU0Qzk0LjA4MDEgMTEyLjI2MiA5NS43MDgxIDExMy44OSA5Ny43MTY0IDExMy44OUgxMDguNjI1QzExMC42MzMgMTEzLjg5IDExMi4yNjEgMTEyLjI2MiAxMTIuMjYxIDExMC4yNTRWOTkuMzQ1M0MxMTIuMjYxIDk3LjMzNyAxMTAuNjMzIDk1LjcwOSAxMDguNjI1IDk1LjcwOVoiIHN0cm9rZT0iI0VDRERGRiIgc3Ryb2tlLXdpZHRoPSI2LjE2ODI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPHBhdGggZD0iTTE1NC45MDYgOTUuNzA5SDE0My45OThDMTQxLjk4OSA5NS43MDkgMTQwLjM2MSA5Ny4zMzcgMTQwLjM2MSA5OS4zNDUzVjExMC4yNTRDMTQwLjM2MSAxMTIuMjYyIDE0MS45ODkgMTEzLjg5IDE0My45OTggMTEzLjg5SDE1NC45MDZDMTU2LjkxNSAxMTMuODkgMTU4LjU0MyAxMTIuMjYyIDE1OC41NDMgMTEwLjI1NFY5OS4zNDUzQzE1OC41NDMgOTcuMzM3IDE1Ni45MTUgOTUuNzA5IDE1NC45MDYgOTUuNzA5WiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSI2LjE2ODI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPHBhdGggZD0iTTEwOC42MjUgMTQxLjk4N0g5Ny43MTY0Qzk1LjcwODEgMTQxLjk4NyA5NC4wODAxIDE0My42MTUgOTQuMDgwMSAxNDUuNjIzVjE1Ni41MzJDOTQuMDgwMSAxNTguNTQgOTUuNzA4MSAxNjAuMTY4IDk3LjcxNjQgMTYwLjE2OEgxMDguNjI1QzExMC42MzMgMTYwLjE2OCAxMTIuMjYxIDE1OC41NCAxMTIuMjYxIDE1Ni41MzJWMTQ1LjYyM0MxMTIuMjYxIDE0My42MTUgMTEwLjYzMyAxNDEuOTg3IDEwOC42MjUgMTQxLjk4N1oiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iNi4xNjgyNCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xNTguNTQzIDE0MS45ODdIMTQ3LjYzNEMxNDUuNzA1IDE0MS45ODcgMTQzLjg1NSAxNDIuNzUzIDE0Mi40OTEgMTQ0LjExN0MxNDEuMTI4IDE0NS40ODEgMTQwLjM2MSAxNDcuMzMxIDE0MC4zNjEgMTQ5LjI1OVYxNjAuMTY4IiBzdHJva2U9IiNFQ0RERkYiIHN0cm9rZS13aWR0aD0iNi4xNjgyNCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xNTguNTQxIDE2MC4xN1YxNjAuMjA4IiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjYuMTY4MjQiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8cGF0aCBkPSJNMTI3LjEzMyAxMTAuNTg1VjEyMS40OTRDMTI3LjEzMyAxMjMuNDIzIDEyNi4zNjYgMTI1LjI3MiAxMjUuMDAyIDEyNi42MzZDMTIzLjYzOSAxMjggMTIxLjc4OSAxMjguNzY2IDExOS44NiAxMjguNzY2SDEwOC45NTEiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iNi4xNjgyNCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik05NC4wODAxIDEyNy4xMTFIOTQuMTE3MiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSI2LjE2ODI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPHBhdGggZD0iTTEyNy4xNDEgOTUuNzA5SDEyNy4xNzgiIHN0cm9rZT0iI0VDRERGRiIgc3Ryb2tlLXdpZHRoPSI2LjE2ODI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPHBhdGggZD0iTTEyNy4xNDEgMTQxLjk4N1YxNDIuMDI0IiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjYuMTY4MjQiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8cGF0aCBkPSJNMTQwLjM2MSAxMjcuMTE1SDE0My42NjciIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iNi4xNjgyNCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xNTguNTQxIDEyNy4xMTVWMTI3LjE1MiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSI2LjE2ODI0IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPHBhdGggZD0iTTEyNy4xNDEgMTYwLjE2OFYxNTYuODYzIiBzdHJva2U9IiNFQ0RERkYiIHN0cm9rZS13aWR0aD0iNi4xNjgyNCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxjaXJjbGUgY3g9IjEyNi40MzciIGN5PSIxMjkuMTYzIiByPSI5My4yODY2IiBzdHJva2U9IiNCN0I3QjciLz4KPGNpcmNsZSBjeD0iMTI2LjQzNyIgY3k9IjEyOS4xNjMiIHI9IjkzLjI4NjYiIHN0cm9rZT0iI0I3QjdCNyIvPgo8Y2lyY2xlIGN4PSIxMjguMDQ0IiBjeT0iMTI3LjU1NSIgcj0iMTI3LjA1IiBzdHJva2U9IiNCN0I3QjciLz4KPGNpcmNsZSBjeD0iMTI4LjA0NCIgY3k9IjEyNy41NTUiIHI9IjEyNy4wNSIgc3Ryb2tlPSIjQjdCN0I3Ii8+CjwvZz4KPGRlZnM+CjxjbGlwUGF0aCBpZD0iY2xpcDBfNDMxOV85MjQzIj4KPHJlY3Qgd2lkdGg9IjI1NS4xIiBoZWlnaHQ9IjI1NS4xIiBmaWxsPSJ3aGl0ZSIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC40OTQxNDEgMC4wMDQ4ODI4MSkiLz4KPC9jbGlwUGF0aD4KPC9kZWZzPgo8L3N2Zz4K" alt="">
  <div>
    <h1 class="font-bold">Payment Links</h1>
    <p class="text-sm">Collect payments easily through Links</p>
  </div>
</div>


<div class=" bg-gray-200 flex p-5 items-center rounded-2xl m-5 gap-7">
<div class>
    <img class="h-5 bg-purple-600" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNzQiIGhlaWdodD0iMjMiIHZpZXdCb3g9IjAgMCA3NCAyMyIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTQ1LjM4NzEgMTAuOTA4QzQ2Ljk3MzQgMTEuMjc0MSA0Ny44NDUgMTIuNTI5MiA0Ny44NDUgMTMuODcxNUM0Ny44NDUgMTYuMjU5NyA0NS43NzA2IDE3LjUzMjIgNDMuMTIwOSAxNy41MzIySDM4LjU4ODVWNC44MDY3NEg0My4wMTYzQzQ1LjQ5MTcgNC44MDY3NCA0Ny4zOTE4IDUuOTM5ODMgNDcuMzkxOCA4LjE4ODU4QzQ3LjM5MTggOS4zNTY1NCA0Ni43OTkxIDEwLjQxOTkgNDUuMzg3MSAxMC45MDhaTTQzLjAxNjMgNi44NjM3M0g0MC45MjQ0VjEwLjAwMTVINDMuMTIwOUM0NC4xODQyIDEwLjAwMTUgNDQuOTg2MSA5LjU0ODI5IDQ0Ljk4NjEgOC40MzI2M0M0NC45ODYxIDcuMzE2OTcgNDQuMTMxOSA2Ljg2MzczIDQzLjAxNjMgNi44NjM3M1pNNDAuOTI0NCAxNS40NzUySDQzLjI0MjlDNDQuNDYzMiAxNS40NzUyIDQ1LjQzOTQgMTQuOTY5NyA0NS40Mzk0IDEzLjc0OTRDNDUuNDM5NCAxMi41MTE4IDQ0LjQ2MzIgMTIuMDQxMSA0My4yNDI5IDEyLjA0MTFINDAuOTI0NFYxNS40NzUyWk00OS44Mzc0IDEyLjY4NjFWNC44MDY3NEg1Mi4xOTA4VjEyLjU2NDFDNTIuMTczNCAxNC4yNzI0IDUzLjAxMDEgMTUuNTc5OCA1NC43MzU5IDE1LjU3OThDNTYuNTMxNCAxNS41Nzk4IDU3LjMxNTggMTQuMjcyNCA1Ny4zMTU4IDEyLjU2NDFWNC44MDY3NEg1OS42NjkyVjEyLjY4NjFDNTkuNjY5MiAxNS41OTczIDU3LjkyNiAxNy43MDY1IDU0LjczNTkgMTcuNzA2NUM1MS42MTU1IDE3LjcwNjUgNDkuODM3NCAxNS41OTczIDQ5LjgzNzQgMTIuNjg2MVpNNjkuODcxMiA0LjgwNjc0SDcyLjUzODRMNjcuOTg4NiAxMi42MzM4VjE3LjUzMjJINjUuNjM1MlYxMi42Njg2TDYxLjA2OCA0LjgwNjc0TDYzLjgwNDggNC44MDY3NEw2NS44NzkzIDguNDMyNjNDNjYuMjI3OSA5LjA0Mjc2IDY2LjU1OTEgOS43MjI2MSA2Ni44MzggMTAuMzY3NkM2Ny4xNTE4IDkuNzA1MTggNjcuNDY1NiA5LjA0Mjc2IDY3Ljc5NjggOC40MzI2M0w2OS44NzEyIDQuODA2NzRaIiBmaWxsPSJ3aGl0ZSIvPgo8cGF0aCBkPSJNMTYuNzAzMyAxOS41NDgyQzE3LjE2MTggMTkuNTQ4MiAxNy41MzM1IDE5LjE3NjQgMTcuNTMzNSAxOC43MTc5QzE3LjUzMzUgMTguMjU5NCAxNy4xNjE4IDE3Ljg4NzcgMTYuNzAzMyAxNy44ODc3QzE2LjI0NDggMTcuODg3NyAxNS44NzMgMTguMjU5NCAxNS44NzMgMTguNzE3OUMxNS44NzMgMTkuMTc2NCAxNi4yNDQ4IDE5LjU0ODIgMTYuNzAzMyAxOS41NDgyWiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjY2MDQ2IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPHBhdGggZD0iTTI1LjgzNjEgMTkuNTQ4MkMyNi4yOTQ2IDE5LjU0ODIgMjYuNjY2MyAxOS4xNzY0IDI2LjY2NjMgMTguNzE3OUMyNi42NjYzIDE4LjI1OTQgMjYuMjk0NiAxNy44ODc3IDI1LjgzNjEgMTcuODg3N0MyNS4zNzc2IDE3Ljg4NzcgMjUuMDA1OSAxOC4yNTk0IDI1LjAwNTkgMTguNzE3OUMyNS4wMDU5IDE5LjE3NjQgMjUuMzc3NiAxOS41NDgyIDI1LjgzNjEgMTkuNTQ4MloiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMS42NjA0NiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xMS43NzE1IDIuOTg1MzVIMTMuNDMxOUwxNS42NDA0IDEzLjI5NjhDMTUuNzIxNCAxMy42NzQ0IDE1LjkzMTUgMTQuMDEyIDE2LjIzNDYgMTQuMjUxNUMxNi41Mzc2IDE0LjQ5MDkgMTYuOTE0NyAxNC42MTcyIDE3LjMwMDggMTQuNjA4NkwyNS40MjA1IDE0LjYwODZDMjUuNzk4NCAxNC42MDggMjYuMTY0OCAxNC40Nzg1IDI2LjQ1OTEgMTQuMjQxNUMyNi43NTM1IDE0LjAwNDUgMjYuOTU4MiAxMy42NzQyIDI3LjAzOTQgMTMuMzA1MUwyOC40MDkzIDcuMTM2NUwxNC4zMjAzIDcuMTM2NSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjY2MDQ2IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPHBhdGggZD0iTTUuNzQ4MDUgOC4wMTI3SDEwLjI4MzgiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMS42NjA0NiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xLjIxNjggMTIuMDU1N0wxMC4yODg0IDEyLjA1NTciIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMS42NjA0NiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+Cjwvc3ZnPgo=" alt="">
</div>  
<div>
    <h1 class="font-bold">Payment Links</h1>
    <p class="text-sm">Collect payments easily through Links</p>
  </div>
</div>
<div class=" bg-gray-200 flex p-5 items-center rounded-2xl m-5 gap-7">
<div class>
    <img class="h-5 bg-purple-600" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNzQiIGhlaWdodD0iMjMiIHZpZXdCb3g9IjAgMCA3NCAyMyIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTQ1LjM4NzEgMTAuOTA4QzQ2Ljk3MzQgMTEuMjc0MSA0Ny44NDUgMTIuNTI5MiA0Ny44NDUgMTMuODcxNUM0Ny44NDUgMTYuMjU5NyA0NS43NzA2IDE3LjUzMjIgNDMuMTIwOSAxNy41MzIySDM4LjU4ODVWNC44MDY3NEg0My4wMTYzQzQ1LjQ5MTcgNC44MDY3NCA0Ny4zOTE4IDUuOTM5ODMgNDcuMzkxOCA4LjE4ODU4QzQ3LjM5MTggOS4zNTY1NCA0Ni43OTkxIDEwLjQxOTkgNDUuMzg3MSAxMC45MDhaTTQzLjAxNjMgNi44NjM3M0g0MC45MjQ0VjEwLjAwMTVINDMuMTIwOUM0NC4xODQyIDEwLjAwMTUgNDQuOTg2MSA5LjU0ODI5IDQ0Ljk4NjEgOC40MzI2M0M0NC45ODYxIDcuMzE2OTcgNDQuMTMxOSA2Ljg2MzczIDQzLjAxNjMgNi44NjM3M1pNNDAuOTI0NCAxNS40NzUySDQzLjI0MjlDNDQuNDYzMiAxNS40NzUyIDQ1LjQzOTQgMTQuOTY5NyA0NS40Mzk0IDEzLjc0OTRDNDUuNDM5NCAxMi41MTE4IDQ0LjQ2MzIgMTIuMDQxMSA0My4yNDI5IDEyLjA0MTFINDAuOTI0NFYxNS40NzUyWk00OS44Mzc0IDEyLjY4NjFWNC44MDY3NEg1Mi4xOTA4VjEyLjU2NDFDNTIuMTczNCAxNC4yNzI0IDUzLjAxMDEgMTUuNTc5OCA1NC43MzU5IDE1LjU3OThDNTYuNTMxNCAxNS41Nzk4IDU3LjMxNTggMTQuMjcyNCA1Ny4zMTU4IDEyLjU2NDFWNC44MDY3NEg1OS42NjkyVjEyLjY4NjFDNTkuNjY5MiAxNS41OTczIDU3LjkyNiAxNy43MDY1IDU0LjczNTkgMTcuNzA2NUM1MS42MTU1IDE3LjcwNjUgNDkuODM3NCAxNS41OTczIDQ5LjgzNzQgMTIuNjg2MVpNNjkuODcxMiA0LjgwNjc0SDcyLjUzODRMNjcuOTg4NiAxMi42MzM4VjE3LjUzMjJINjUuNjM1MlYxMi42Njg2TDYxLjA2OCA0LjgwNjc0TDYzLjgwNDggNC44MDY3NEw2NS44NzkzIDguNDMyNjNDNjYuMjI3OSA5LjA0Mjc2IDY2LjU1OTEgOS43MjI2MSA2Ni44MzggMTAuMzY3NkM2Ny4xNTE4IDkuNzA1MTggNjcuNDY1NiA5LjA0Mjc2IDY3Ljc5NjggOC40MzI2M0w2OS44NzEyIDQuODA2NzRaIiBmaWxsPSJ3aGl0ZSIvPgo8cGF0aCBkPSJNMTYuNzAzMyAxOS41NDgyQzE3LjE2MTggMTkuNTQ4MiAxNy41MzM1IDE5LjE3NjQgMTcuNTMzNSAxOC43MTc5QzE3LjUzMzUgMTguMjU5NCAxNy4xNjE4IDE3Ljg4NzcgMTYuNzAzMyAxNy44ODc3QzE2LjI0NDggMTcuODg3NyAxNS44NzMgMTguMjU5NCAxNS44NzMgMTguNzE3OUMxNS44NzMgMTkuMTc2NCAxNi4yNDQ4IDE5LjU0ODIgMTYuNzAzMyAxOS41NDgyWiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjY2MDQ2IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPHBhdGggZD0iTTI1LjgzNjEgMTkuNTQ4MkMyNi4yOTQ2IDE5LjU0ODIgMjYuNjY2MyAxOS4xNzY0IDI2LjY2NjMgMTguNzE3OUMyNi42NjYzIDE4LjI1OTQgMjYuMjk0NiAxNy44ODc3IDI1LjgzNjEgMTcuODg3N0MyNS4zNzc2IDE3Ljg4NzcgMjUuMDA1OSAxOC4yNTk0IDI1LjAwNTkgMTguNzE3OUMyNS4wMDU5IDE5LjE3NjQgMjUuMzc3NiAxOS41NDgyIDI1LjgzNjEgMTkuNTQ4MloiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMS42NjA0NiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xMS43NzE1IDIuOTg1MzVIMTMuNDMxOUwxNS42NDA0IDEzLjI5NjhDMTUuNzIxNCAxMy42NzQ0IDE1LjkzMTUgMTQuMDEyIDE2LjIzNDYgMTQuMjUxNUMxNi41Mzc2IDE0LjQ5MDkgMTYuOTE0NyAxNC42MTcyIDE3LjMwMDggMTQuNjA4NkwyNS40MjA1IDE0LjYwODZDMjUuNzk4NCAxNC42MDggMjYuMTY0OCAxNC40Nzg1IDI2LjQ1OTEgMTQuMjQxNUMyNi43NTM1IDE0LjAwNDUgMjYuOTU4MiAxMy42NzQyIDI3LjAzOTQgMTMuMzA1MUwyOC40MDkzIDcuMTM2NUwxNC4zMjAzIDcuMTM2NSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjY2MDQ2IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPHBhdGggZD0iTTUuNzQ4MDUgOC4wMTI3SDEwLjI4MzgiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMS42NjA0NiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xLjIxNjggMTIuMDU1N0wxMC4yODg0IDEyLjA1NTciIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMS42NjA0NiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+Cjwvc3ZnPgo=" alt="">
</div>  

<div>
    <h1 class="font-bold">Payment Links</h1>
    <p class="text-sm">Collect payments easily through Links</p>
  </div>
</div>

</div>

<div class="sm:pt-5 sm:pl-5 sm:pr-5 lg:px-60 ">
  <div class="h-auto -z-10 top-10 flex justify-center items-center  text-black  rounded-3xl flex-col p-10">
    <img class="h-12 " src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTU0IiBoZWlnaHQ9IjE2MSIgdmlld0JveD0iMCAwIDE1NCAxNjEiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxnIGNsaXAtcGF0aD0idXJsKCNjbGlwMF80MzE1Xzg3MTUpIj4KPGNpcmNsZSBjeD0iNzAuMjg2NiIgY3k9IjcwLjc3MTkiIHI9IjY5Ljk2MDQiIGZpbGw9IiNGNENDN0MiLz4KPGNpcmNsZSBjeD0iNjkuNTc2MiIgY3k9IjcwLjA0ODgiIHI9IjQ3LjgzMDEiIGZpbGw9IiNGRkRFOUYiLz4KPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik03OS45MjkyIDU0Ljc4MlY1OS43NTU1SDg1Ljk5NjdWNjQuNDM5MUg3OS43NTA4Qzc5LjI3NTIgNjcuOTA5MiA3Ny43Nzc3IDcwLjUzMTcgNzUuMjU5MSA3Mi4zMDM5QzcyLjc0MDUgNzQuMDc3OSA2OC45MDI4IDc0Ljk2NCA2My43NDc3IDc0Ljk2NFY3OC42MDc1QzYzLjc0NzcgODIuNjE3OCA2NS40NTI4IDg0LjYyMjEgNjguODY0MSA4NC42MjIxQzcwLjUyOTYgODQuNjIyMSA3MS43Njg2IDg0LjEyMTIgNzIuNTgyIDgzLjExNzdDNzMuMzk0NSA4Mi4xMTYxIDczLjgwMjEgODAuNjEyNiA3My44MDIxIDc4LjYwNzVIODEuNTk0N0M4MS40MzYxIDgyLjQyNDMgODAuMzA1NyA4NS40MDI3IDc4LjIwNDIgODcuNTQxOEM3Ni4xMDE4IDg5LjY4MTggNzMuMTA3NiA5MC43NTEzIDY5LjIyMDggOTAuNzUxM0M2NC44OTggOTAuNzUxMyA2MS41OTYyIDg5LjY0MzMgNTkuMzE1NCA4Ny40MjYyQzU3LjAzNDcgODUuMjEgNTUuODk0OCA4MS44ODQ5IDU1Ljg5NDggNzcuNDUwOFY2OS42NDM4QzYwLjIxNzYgNjkuNjQzOCA2My40NTA0IDY5LjUxOSA2NS41OTE2IDY5LjI2NzdDNjcuNzMzNiA2OS4wMTgyIDY5LjI2OTkgNjguNTI2NSA3MC4yMDIyIDY3Ljc5MzZDNzEuMTMzNSA2Ny4wNjE2IDcxLjcxOTUgNjUuOTQyNiA3MS45NTczIDY0LjQzOTFINTQuNTg1OVY1OS43NTU1SDcyLjA3NjJWNTQuNzgySDU0LjU4NTlWNDkuMzQ2Mkg4NS45OTY3VjU0Ljc4Mkg3OS45MjkyWiIgZmlsbD0iIzJDMTY0NSIvPgo8Y2lyY2xlIGN4PSIxMTQuNjYxIiBjeT0iMTIxLjkwOCIgcj0iMzYuNzQ4OSIgZmlsbD0iIzg5NUFFOCIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIzLjQ1NzQ4Ii8+CjxwYXRoIGQ9Ik0xMTEuNzMgMTIzLjM3M0MxMTIuMzYgMTI0LjIxNSAxMTMuMTYzIDEyNC45MTEgMTE0LjA4NSAxMjUuNDE1QzExNS4wMDcgMTI1LjkxOSAxMTYuMDI3IDEyNi4yMTkgMTE3LjA3NiAxMjYuMjk0QzExOC4xMjQgMTI2LjM2OSAxMTkuMTc2IDEyNi4yMTcgMTIwLjE2IDEyNS44NUMxMjEuMTQ1IDEyNS40ODMgMTIyLjAzOSAxMjQuOTA4IDEyMi43ODIgMTI0LjE2NUwxMjcuMTc5IDExOS43NjhDMTI4LjUxNCAxMTguMzg1IDEyOS4yNTMgMTE2LjUzNCAxMjkuMjM2IDExNC42MTNDMTI5LjIyIDExMi42OTEgMTI4LjQ0OSAxMTAuODUzIDEyNy4wOSAxMDkuNDk0QzEyNS43MzEgMTA4LjEzNSAxMjMuODkzIDEwNy4zNjUgMTIxLjk3MiAxMDcuMzQ4QzEyMC4wNSAxMDcuMzMxIDExOC4xOTkgMTA4LjA3IDExNi44MTcgMTA5LjQwNUwxMTQuMjk2IDExMS45MTEiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMi45MzE0OCIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xMTcuNTkyIDEyMC40NTRDMTE2Ljk2MyAxMTkuNjEyIDExNi4xNiAxMTguOTE2IDExNS4yMzcgMTE4LjQxMkMxMTQuMzE1IDExNy45MDggMTEzLjI5NSAxMTcuNjA4IDExMi4yNDcgMTE3LjUzM0MxMTEuMTk5IDExNy40NTggMTEwLjE0NyAxMTcuNjEgMTA5LjE2MiAxMTcuOTc3QzEwOC4xNzcgMTE4LjM0NCAxMDcuMjgzIDExOC45MTkgMTA2LjU0IDExOS42NjJMMTAyLjE0MyAxMjQuMDU5QzEwMC44MDggMTI1LjQ0MiAxMDAuMDcgMTI3LjI5MyAxMDAuMDg2IDEyOS4yMTRDMTAwLjEwMyAxMzEuMTM2IDEwMC44NzQgMTMyLjk3NCAxMDIuMjMyIDEzNC4zMzNDMTAzLjU5MSAxMzUuNjkyIDEwNS40MjkgMTM2LjQ2MiAxMDcuMzUxIDEzNi40NzlDMTA5LjI3MyAxMzYuNDk2IDExMS4xMjQgMTM1Ljc1NyAxMTIuNTA2IDEzNC40MjJMMTE1LjAxMiAxMzEuOTE2IiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjIuOTMxNDgiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L2c+CjxkZWZzPgo8Y2xpcFBhdGggaWQ9ImNsaXAwXzQzMTVfODcxNSI+CjxyZWN0IHdpZHRoPSIxNTIuODEzIiBoZWlnaHQ9IjE1OS41NzQiIGZpbGw9IndoaXRlIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjMyNjE3MiAwLjgxMTUyMykiLz4KPC9jbGlwUGF0aD4KPC9kZWZzPgo8L3N2Zz4K" alt="">

    <h1 class="text-2xl font-bold mt-3">Simple, Transparent</h1>
    <h1 class="text-2xl font-bold text-purple-500">Pricing</h1>
    <div class="bg-white w-full flex justify-center mt-10 flex-col items-center px-18">
      <h1 class=" bg-cyan-600 p-2 text-xs rounded-xl">Limited period Offer</h1>
      <h1 class="mt-5 text-2xl">Standard Plan</h1>
      <h1 class="text-5xl font-extrabold"><span class="line-through text-gray-400 text-lg">2%</span>    Free*</h1>
      <div class="flex items-center mt-5 gap-3 text-xs">
        <img class="h-5" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjkiIGhlaWdodD0iMjgiIHZpZXdCb3g9IjAgMCAyOSAyOCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTE0LjY3MjQgMjUuNTU1N0MyMS4wODY3IDI1LjU1NTcgMjYuMjg2MiAyMC4zNTYyIDI2LjI4NjIgMTMuOTQxOUMyNi4yODYyIDcuNTI3NjIgMjEuMDg2NyAyLjMyODEyIDE0LjY3MjQgMi4zMjgxMkM4LjI1ODA5IDIuMzI4MTIgMy4wNTg1OSA3LjUyNzYyIDMuMDU4NTkgMTMuOTQxOUMzLjA1ODU5IDIwLjM1NjIgOC4yNTgwOSAyNS41NTU3IDE0LjY3MjQgMjUuNTU1N1oiIHN0cm9rZT0iYmxhY2siIHN0cm9rZS13aWR0aD0iMi4zMjI3NiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xMS4xOTE0IDEzLjk0MzlMMTMuNTE0MiAxNi4yNjY2TDE4LjE1OTcgMTEuNjIxMSIgc3Ryb2tlPSJibGFjayIgc3Ryb2tlLXdpZHRoPSIyLjMyMjc2IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==" alt="">
        <h2>Zero hidden charges</h2>
      </div>
      <div class="flex items-center mt-5 gap-3 text-xs">
        <img class="h-5" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjkiIGhlaWdodD0iMjgiIHZpZXdCb3g9IjAgMCAyOSAyOCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTE0LjY3MjQgMjUuNTU1N0MyMS4wODY3IDI1LjU1NTcgMjYuMjg2MiAyMC4zNTYyIDI2LjI4NjIgMTMuOTQxOUMyNi4yODYyIDcuNTI3NjIgMjEuMDg2NyAyLjMyODEyIDE0LjY3MjQgMi4zMjgxMkM4LjI1ODA5IDIuMzI4MTIgMy4wNTg1OSA3LjUyNzYyIDMuMDU4NTkgMTMuOTQxOUMzLjA1ODU5IDIwLjM1NjIgOC4yNTgwOSAyNS41NTU3IDE0LjY3MjQgMjUuNTU1N1oiIHN0cm9rZT0iYmxhY2siIHN0cm9rZS13aWR0aD0iMi4zMjI3NiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xMS4xOTE0IDEzLjk0MzlMMTMuNTE0MiAxNi4yNjY2TDE4LjE1OTcgMTEuNjIxMSIgc3Ryb2tlPSJibGFjayIgc3Ryb2tlLXdpZHRoPSIyLjMyMjc2IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==" alt="">
        <h2>Zero Setup Fee</h2>
      </div>
      <div class="flex items-center mt-5 gap-3 text-xs">
        <img class="h-5" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjkiIGhlaWdodD0iMjgiIHZpZXdCb3g9IjAgMCAyOSAyOCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTE0LjY3MjQgMjUuNTU1N0MyMS4wODY3IDI1LjU1NTcgMjYuMjg2MiAyMC4zNTYyIDI2LjI4NjIgMTMuOTQxOUMyNi4yODYyIDcuNTI3NjIgMjEuMDg2NyAyLjMyODEyIDE0LjY3MjQgMi4zMjgxMkM4LjI1ODA5IDIuMzI4MTIgMy4wNTg1OSA3LjUyNzYyIDMuMDU4NTkgMTMuOTQxOUMzLjA1ODU5IDIwLjM1NjIgOC4yNTgwOSAyNS41NTU3IDE0LjY3MjQgMjUuNTU1N1oiIHN0cm9rZT0iYmxhY2siIHN0cm9rZS13aWR0aD0iMi4zMjI3NiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik0xMS4xOTE0IDEzLjk0MzlMMTMuNTE0MiAxNi4yNjY2TDE4LjE1OTcgMTEuNjIxMSIgc3Ryb2tlPSJibGFjayIgc3Ryb2tlLXdpZHRoPSIyLjMyMjc2IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==" alt="">
        <h2>Zero annual maintenance fee</h2>
      </div>
    </div>
  </div>
</div>



<div class="flex sm:p-3 sm:items-center sm:justify-center sm:w-svw">
      <div class="bg-purple-700 text-xs rounded-3xl items-center justify-center p-3 px-9 text-white">GET STARTED FOR FREE</div>    
</div>

<div class="flex justify-center">
  <img src="https://www.phonepe.com/webstatic/6992/static/76748761aa1c1a7a3cff5a5044c4a929/41c62/trusted-pg-mobile.webp" alt="">
</div>


<div class="p-5 flex sm:flex-col gap-10 lg:flex-row items-center">
  <div class="flex flex-col text-center  gap-3 lg:gap-7">
    <img class="h-10 lg:h-20" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTEzIiBoZWlnaHQ9IjExMSIgdmlld0JveD0iMCAwIDExMyAxMTEiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHg9IjAuNDA2MjUiIHk9IjAuNDU3MDMxIiB3aWR0aD0iMTEyIiBoZWlnaHQ9IjExMC4yOSIgcng9IjI2IiBmaWxsPSJ1cmwoI3BhaW50MF9saW5lYXJfNDMxNV84Mjc1KSIvPgo8cGF0aCBkPSJNNDQuMDA1NSA0MS40OTYxTDI2LjkwNjIgNTguNTk1M0w0NC4wMDU1IDc1LjY5NDYiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iOCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8cGF0aCBkPSJNNjUuMzg1MSA0MS40OTYxTDgyLjQ4NDQgNTguNTk1M0w2NS4zODUxIDc1LjY5NDYiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iOCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8ZGVmcz4KPGxpbmVhckdyYWRpZW50IGlkPSJwYWludDBfbGluZWFyXzQzMTVfODI3NSIgeDE9IjkuMzgzMzUiIHkxPSIwLjQ1NzAzIiB4Mj0iNTYuNDA2MyIgeTI9IjExMC43NDciIGdyYWRpZW50VW5pdHM9InVzZXJTcGFjZU9uVXNlIj4KPHN0b3Agc3RvcC1jb2xvcj0iIzQ2QzU4OCIvPgo8c3RvcCBvZmZzZXQ9IjEiIHN0b3AtY29sb3I9IiM2Q0FGRUMiLz4KPC9saW5lYXJHcmFkaWVudD4KPC9kZWZzPgo8L3N2Zz4K" alt="">
    <h1 class=" text-gray-500 lg:text-3xl">DEVELOPERS</h1>
    <h1 class="font-bold lg:text-5xl">Integrated Ecosystem for Developers</h1>
    <p class="text-xs lg:text-sm">PhonePe Payment Gateway provides low-code SDKs and RESTful APIs that work quickly with existing apps and ecosystems. Easily integrate PhonePe Payment Gateway into your tech stack.</p>
    <button class="sm:hidden lg:flex bg-purple-600 p-3 text-white shadow-black mr-auto rounded-md">View Documentation</button>
  </div>
  <div>
    <img src="https://www.phonepe.com/webstatic/6992/static/40e738e0d6cc7a1f6950c00ae45a609a/c0886/pg_developer_image_mobile.png" alt="">
    
  </div>
</div>

<div class="sm:flex  justify-center lg:hidden w-60 mx-auto bg-purple-600 text-white rounded-2xl px-5 py-3">
  <button>View Documentation</button>
</div>

<h1 class="flex justify-center mt-10 mb-0 text-2xl font-bold">Supports Extensive Platforms</h1>

<div class="bg-purple-400 m-5 rounded-xl">
  <div class=" flex justify-center  gap-10 pt-10">
  <img class="sm:h-24 lg:h-32" src="https://www.phonepe.com/static/pg_platforms_icon_react_native-a17d0ae569f059f26a8c850601ffd888.png" alt="">
  <img class="sm:h-24 lg:h-32" src="https://www.phonepe.com/static/pg_platforms_icon_android-a87526a054063d97f496972637a5c5aa.png" alt="">
</div>
<div class="flex justify-center gap-10">
  <img class="sm:h-24 lg:h-32" src="https://www.phonepe.com/static/pg_platforms_icon_php-81b5cde1badf68c10992c73cb7c161d8.png" alt="">
  <img class="sm:h-24 lg:h-32" src="https://www.phonepe.com/static/pg_platforms_icon_ios-06270f89fbc60bd7b292355b3e6c9a87.png" alt="">
  <img class="sm:h-24 lg:h-32" src="https://www.phonepe.com/static/pg_platforms_icon_c_hash-22072164c63dbffa4ac3ebca54f62096.png" alt="">
</div>
<div class=" flex justify-center gap-10 pb-10">
  <img class="sm:h-24 lg:h-32" src="https://www.phonepe.com/static/pg_platforms_icon_python-ede7bb4de427da8c7ceaabdb84b46ab8.png" alt="">
  <img class="sm:h-24 lg:h-32" src="https://www.phonepe.com/static/pg_platforms_icon_java-940cbb85ca9c57e8379fcb772568d51b.png" alt="">
</div>
</div>



<h1 class="flex justify-center font-bold text-xl my-10">Plugins</h1>

<div class="lg:flex justify-center">
  <div class="flex items-center justify-center bg-gray-300 sm:px-5 sm:py-5 lg:px-10 lg:py-16 m-5 rounded-2xl">
  <img class="h-10" src="https://www.phonepe.com/static/pg_platform_plugins_icon_shopify-2cf187e0e4b1982ce8034ae5e76738ae.svg" alt="">
  <img class="h-8" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDMiIGhlaWdodD0iNDMiIHZpZXdCb3g9IjAgMCA0MyA0MyIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTkuMDMxMjUgMjEuNzQ2MUwzMy43OCAyMS43NDYxIiBzdHJva2U9IiMyMzIwMjgiIHN0cm9rZS13aWR0aD0iMi42MjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8cGF0aCBkPSJNMjEuNDA1NiAzNC4xMjA1TDMzLjc4IDIxLjc0NjFMMjEuNDA1NiA5LjM3MTczIiBzdHJva2U9IiMyMzIwMjgiIHN0cm9rZS13aWR0aD0iMi42MjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L3N2Zz4K" alt="">
</div>
<div class="flex items-center justify-center bg-gray-300 sm:px-5 sm:py-5 lg:px-10 lg:py-16 m-5 rounded-2xl">
  <img class="h-8" src="https://www.phonepe.com/static/pg_platform_plugins_icon_opencart_mobile-88414f41376ba38c8e8dd4edbc9ae382.svg" alt="">
  <img class="h-8" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDMiIGhlaWdodD0iNDMiIHZpZXdCb3g9IjAgMCA0MyA0MyIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTkuMDMxMjUgMjEuNzQ2MUwzMy43OCAyMS43NDYxIiBzdHJva2U9IiMyMzIwMjgiIHN0cm9rZS13aWR0aD0iMi42MjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8cGF0aCBkPSJNMjEuNDA1NiAzNC4xMjA1TDMzLjc4IDIxLjc0NjFMMjEuNDA1NiA5LjM3MTczIiBzdHJva2U9IiMyMzIwMjgiIHN0cm9rZS13aWR0aD0iMi42MjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L3N2Zz4K" alt="">
</div>
<div class="flex items-center justify-center bg-gray-300 sm:px-5 sm:py-5 lg:px-10 lg:py-16 rounded-2xl m-5">
  <img class="h-10" src="https://www.phonepe.com/static/pg_platform_plugins_icon_woo-bbb0a1b628efe76e2d492673358f4f7c.svg" alt="">
  <img class="h-8" src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDMiIGhlaWdodD0iNDMiIHZpZXdCb3g9IjAgMCA0MyA0MyIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTkuMDMxMjUgMjEuNzQ2MUwzMy43OCAyMS43NDYxIiBzdHJva2U9IiMyMzIwMjgiIHN0cm9rZS13aWR0aD0iMi42MjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8cGF0aCBkPSJNMjEuNDA1NiAzNC4xMjA1TDMzLjc4IDIxLjc0NjFMMjEuNDA1NiA5LjM3MTczIiBzdHJva2U9IiMyMzIwMjgiIHN0cm9rZS13aWR0aD0iMi42MjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L3N2Zz4K" alt="">
</div>
</div>

<div class="lg:hidden">
  <div class=" bg-blue-700 mt-28 text-white flex justify-center text-center sm:flex-col">
    <div class="lg:flex lg:flex-col lg:mx-auto lg:justify-center lg:items-center">
      <h1 class="font-bold py-10">Light SDKs, Flexible APIs</h1>
      <p class="text-xs flex  w-10/12 mx-auto mb-10">Grow your business with well-documented and lightweight SDKs, simple-to-use and flexible APIs that provide an effortless way to initiate and authorize your payments, and more. Choose the integration that's right for you, and we'll help you get started in no time!</p>
      <div class="flex sm:p-3 sm:items-center sm:justify-center sm:w-svw">
          <div class="bg-white text-xs rounded-3xl items-center justify-center p-3 px-9 sm:hidden text-black font-bold">GET STARTED FOR FREE</div>    
      </div>
    </div>  
  </div>
  <div class="flex">
    <img class="flex" src="https://www.phonepe.com/webstatic/6992/static/3ee897131a34021ce26bc2da2f803963/bc8e0/pg_sdk_img_mobile.png" alt="">
  </div>
  <div class="flex sm:p-3 sm:items-center sm:justify-center sm:w-svw">
      <div class="bg-purple-500 text-xs rounded-3xl items-center justify-center p-3 px-9 text-white font-bold">GET STARTED FOR FREE</div>    
  </div>
</div>

<div class="lg:flex sm:hidden ">
  <div class="sm:hidden lg:flex bg-blue-700 text-white p-10 flex-col w-8/12  gap-10">
    <h1 class="font-extra-bold text-5xl">Light SDKs, <br> Flexible APIs</h1>
    <p>Grow your business with well-documented and lightweight SDKs, simple-to-use and flexible APIs that provide an effortless way to initiate and authorize your payments, and more. Choose the integration that's right for you, and we'll help you get started in no time!</p>
    <h1 class="bg-white text-black p-3 w-fit rounded-3xl font-bold px-10">Get Started for Free</h1>
  </div>  
  <div class="">
    <img class="" src="https://www.phonepe.com/webstatic/6992/static/3ee897131a34021ce26bc2da2f803963/bc8e0/pg_sdk_img_mobile.png" alt="">
  </div>
</div>


<div>
  <h1 class="my-10 font-bold flex justify-center text-2xl">Frequently Asked Questions</h1>
</div>

<div class="p-10 flex flex-col font-bold gap-10 ">
  <h1>What is the PhonePe Payment Gateway advantage?</h1>
  <h1>What additional features do I get with PhonePe Payment Gateway?</h1>
  <h1>How do I integrate PhonePe Payment Gateway with my website?</h1>
  <h1>How do I integrate PhonePe Payment Gateway with my mobile application?</h1>
  <h1>Are there plugins available for major E-commerce Platforms?</h1>
</div>


<div class=" bg-purple-500 lg:hidden flex justify-center flex-col gap-5 p-5">
  <img class="h-auto" src="https://www.phonepe.com/webstatic/7083/static/40b795ce6ab0d486a53a5b7e72732415/5f3b8/pg_footer_logo_mobile.png" alt="">
  <h1 class="text-white text-2xl">Sign up for PhonePe Payment Gateway now and start accepting payments instantly</h1>
  <div class="flex items-center gap-3">
    <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjUiIGhlaWdodD0iMjUiIHZpZXdCb3g9IjAgMCAyNSAyNSIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEyLjkzMzYgMjIuMTU2MkMxOC40NTY2IDIyLjE1NjIgMjIuOTMzNiAxNy42NzkyIDIyLjkzMzYgMTIuMTU2MkMyMi45MzM2IDYuNjMzMjUgMTguNDU2NiAyLjE1NjI1IDEyLjkzMzYgMi4xNTYyNUM3LjQxMDU5IDIuMTU2MjUgMi45MzM1OSA2LjYzMzI1IDIuOTMzNTkgMTIuMTU2MkMyLjkzMzU5IDE3LjY3OTIgNy40MTA1OSAyMi4xNTYyIDEyLjkzMzYgMjIuMTU2MloiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik05LjkzMzU5IDEyLjE1NjJMMTEuOTMzNiAxNC4xNTYyTDE1LjkzMzYgMTAuMTU2MiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==" alt="">
    <h1 class="text-white text-2xl">Easy Onboarding</h1>
  </div>
  <div class="flex items-center gap-3">
    <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjUiIGhlaWdodD0iMjUiIHZpZXdCb3g9IjAgMCAyNSAyNSIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEyLjkzMzYgMjIuMTU2MkMxOC40NTY2IDIyLjE1NjIgMjIuOTMzNiAxNy42NzkyIDIyLjkzMzYgMTIuMTU2MkMyMi45MzM2IDYuNjMzMjUgMTguNDU2NiAyLjE1NjI1IDEyLjkzMzYgMi4xNTYyNUM3LjQxMDU5IDIuMTU2MjUgMi45MzM1OSA2LjYzMzI1IDIuOTMzNTkgMTIuMTU2MkMyLjkzMzU5IDE3LjY3OTIgNy40MTA1OSAyMi4xNTYyIDEyLjkzMzYgMjIuMTU2MloiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik05LjkzMzU5IDEyLjE1NjJMMTEuOTMzNiAxNC4xNTYyTDE1LjkzMzYgMTAuMTU2MiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==" alt="">
    <h1 class="text-white text-2xl">Developer friendly APIs</h1>
  </div>
  <div class="flex items-center gap-3">
    <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjUiIGhlaWdodD0iMjUiIHZpZXdCb3g9IjAgMCAyNSAyNSIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEyLjkzMzYgMjIuMTU2MkMxOC40NTY2IDIyLjE1NjIgMjIuOTMzNiAxNy42NzkyIDIyLjkzMzYgMTIuMTU2MkMyMi45MzM2IDYuNjMzMjUgMTguNDU2NiAyLjE1NjI1IDEyLjkzMzYgMi4xNTYyNUM3LjQxMDU5IDIuMTU2MjUgMi45MzM1OSA2LjYzMzI1IDIuOTMzNTkgMTIuMTU2MkMyLjkzMzU5IDE3LjY3OTIgNy40MTA1OSAyMi4xNTYyIDEyLjkzMzYgMjIuMTU2MloiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik05LjkzMzU5IDEyLjE1NjJMMTEuOTMzNiAxNC4xNTYyTDE1LjkzMzYgMTAuMTU2MiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==" alt="">
    <h1 class="text-white text-2xl">Robust Support</h1>
  </div>
  <div class="flex sm:p-3 sm:items-center sm:justify-center sm:w-svw">
      <div class="bg-white text-xs rounded-3xl items-center justify-center p-3 px-9 text-black font-bold">GET STARTED FOR FREE</div>    
  </div>
</div>



<div class="lg:flex bg-purple-500 p-16 items-center sm:hidden">
  <div class="flex flex-col gap-10 w-1/2">
    <h1 class="text-white text-2xl">Sign up for PhonePe Payment Gateway now and start accepting payments instantly</h1>
    <div class="flex items-center gap-3">
      <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjUiIGhlaWdodD0iMjUiIHZpZXdCb3g9IjAgMCAyNSAyNSIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEyLjkzMzYgMjIuMTU2MkMxOC40NTY2IDIyLjE1NjIgMjIuOTMzNiAxNy42NzkyIDIyLjkzMzYgMTIuMTU2MkMyMi45MzM2IDYuNjMzMjUgMTguNDU2NiAyLjE1NjI1IDEyLjkzMzYgMi4xNTYyNUM3LjQxMDU5IDIuMTU2MjUgMi45MzM1OSA2LjYzMzI1IDIuOTMzNTkgMTIuMTU2MkMyLjkzMzU5IDE3LjY3OTIgNy40MTA1OSAyMi4xNTYyIDEyLjkzMzYgMjIuMTU2MloiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik05LjkzMzU5IDEyLjE1NjJMMTEuOTMzNiAxNC4xNTYyTDE1LjkzMzYgMTAuMTU2MiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==" alt="">
      <h1 class="text-white text-2xl">Easy Onboarding</h1>
    </div>
    <div class="flex items-center gap-3">
      <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjUiIGhlaWdodD0iMjUiIHZpZXdCb3g9IjAgMCAyNSAyNSIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEyLjkzMzYgMjIuMTU2MkMxOC40NTY2IDIyLjE1NjIgMjIuOTMzNiAxNy42NzkyIDIyLjkzMzYgMTIuMTU2MkMyMi45MzM2IDYuNjMzMjUgMTguNDU2NiAyLjE1NjI1IDEyLjkzMzYgMi4xNTYyNUM3LjQxMDU5IDIuMTU2MjUgMi45MzM1OSA2LjYzMzI1IDIuOTMzNTkgMTIuMTU2MkMyLjkzMzU5IDE3LjY3OTIgNy40MTA1OSAyMi4xNTYyIDEyLjkzMzYgMjIuMTU2MloiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik05LjkzMzU5IDEyLjE1NjJMMTEuOTMzNiAxNC4xNTYyTDE1LjkzMzYgMTAuMTU2MiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==" alt="">
      <h1 class="text-white text-2xl">Developer friendly APIs</h1>
    </div>
    <div class="flex items-center gap-3">
      <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjUiIGhlaWdodD0iMjUiIHZpZXdCb3g9IjAgMCAyNSAyNSIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTEyLjkzMzYgMjIuMTU2MkMxOC40NTY2IDIyLjE1NjIgMjIuOTMzNiAxNy42NzkyIDIyLjkzMzYgMTIuMTU2MkMyMi45MzM2IDYuNjMzMjUgMTguNDU2NiAyLjE1NjI1IDEyLjkzMzYgMi4xNTYyNUM3LjQxMDU5IDIuMTU2MjUgMi45MzM1OSA2LjYzMzI1IDIuOTMzNTkgMTIuMTU2MkMyLjkzMzU5IDE3LjY3OTIgNy40MTA1OSAyMi4xNTYyIDEyLjkzMzYgMjIuMTU2MloiIHN0cm9rZT0id2hpdGUiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+CjxwYXRoIGQ9Ik05LjkzMzU5IDEyLjE1NjJMMTEuOTMzNiAxNC4xNTYyTDE1LjkzMzYgMTAuMTU2MiIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIyIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KPC9zdmc+Cg==" alt="">
      <h1 class="text-white text-2xl">Robust Support</h1>
    </div>
    <div class="flex sm:p-3 sm:items-center sm:justify-center sm:w-svw">
        <div class="bg-white text-xs rounded-3xl mr-auto p-3 px-9  text-black font-bold">GET STARTED FOR FREE</div>    
    </div>
  </div>

  <div>
    <img class="h-96 flex" src="https://www.phonepe.com/webstatic/7083/static/e4d037ac9efcdc021bf62e762da85bd7/61a07/pg_footer_logo_desktop.png" alt="">
  </div>
</div>

<div class="lg:hidden">
  <img class="h-16 m-5 mb-10" src="data:image/svg+xml;base64,PHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSJMYXllcl8yIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHg9IjAiIHk9IjAiIHZpZXdCb3g9IjAgMCAxMzIgNDgiIHhtbDpzcGFjZT0icHJlc2VydmUiPjxzdHlsZT4uc3Qwe2ZpbGw6IzVmMjU5Zn08L3N0eWxlPjxjaXJjbGUgdHJhbnNmb3JtPSJyb3RhdGUoLTc2LjcxNCAxNy44NyAyNC4wMDEpIiBjbGFzcz0ic3QwIiBjeD0iMTcuOSIgY3k9IjI0IiByPSIxNy45Ii8+PHBhdGggY2xhc3M9InN0MCIgZD0iTTkwLjUgMzQuMnYtNi41YzAtMS42LS42LTIuNC0yLjEtMi40LS42IDAtMS4zLjEtMS43LjJWMzVjMCAuMy0uMy42LS42LjZoLTIuM2MtLjMgMC0uNi0uMy0uNi0uNlYyMy45YzAtLjQuMy0uNy42LS44IDEuNS0uNSAzLS44IDQuNi0uOCAzLjYgMCA1LjYgMS45IDUuNiA1LjR2Ny40YzAgLjMtLjMuNi0uNi42SDkyYy0uOSAwLTEuNS0uNy0xLjUtMS41em05LTMuOWwtLjEuOWMwIDEuMi44IDEuOSAyLjEgMS45IDEgMCAxLjktLjMgMi45LS44LjEgMCAuMi0uMS4zLS4xLjIgMCAuMy4xLjQuMi4xLjEuMy40LjMuNC4yLjMuNC43LjQgMSAwIC41LS4zIDEtLjcgMS4yLTEuMS42LTIuNC45LTMuOC45LTEuNiAwLTIuOS0uNC0zLjktMS4yLTEtLjktMS42LTIuMS0xLjYtMy42di0zLjljMC0zLjEgMi01IDUuNC01IDMuMyAwIDUuMiAxLjggNS4yIDV2Mi40YzAgLjMtLjMuNi0uNi42aC02LjN6bS0uMS0yLjJIMTAzLjJ2LTFjMC0xLjItLjctMi0xLjktMnMtMS45LjctMS45IDJ2MXptMjUuNSAyLjJsLS4xLjljMCAxLjIuOCAxLjkgMi4xIDEuOSAxIDAgMS45LS4zIDIuOS0uOC4xIDAgLjItLjEuMy0uMS4yIDAgLjMuMS40LjIuMS4xLjMuNC4zLjQuMi4zLjQuNy40IDEgMCAuNS0uMyAxLS43IDEuMi0xLjEuNi0yLjQuOS0zLjguOS0xLjYgMC0yLjktLjQtMy45LTEuMi0xLS45LTEuNi0yLjEtMS42LTMuNnYtMy45YzAtMy4xIDItNSA1LjQtNSAzLjMgMCA1LjIgMS44IDUuMiA1djIuNGMwIC4zLS4zLjYtLjYuNmgtNi4zem0tLjEtMi4ySDEyOC42di0xYzAtMS4yLS43LTItMS45LTJzLTEuOS43LTEuOSAydjF6TTY2IDM1LjdoMS40Yy4zIDAgLjYtLjMuNi0uNnYtNy40YzAtMy40LTEuOC01LjQtNC44LTUuNC0uOSAwLTEuOS4yLTIuNS40VjE5YzAtLjgtLjctMS41LTEuNS0xLjVoLTEuNGMtLjMgMC0uNi4zLS42LjZ2MTdjMCAuMy4zLjYuNi42aDIuM2MuMyAwIC42LS4zLjYtLjZ2LTkuNGMuNS0uMiAxLjItLjMgMS43LS4zIDEuNSAwIDIuMS43IDIuMSAyLjR2Ni41Yy4xLjcuNyAxLjQgMS41IDEuNHptMTUuMS04LjRWMzFjMCAzLjEtMi4xIDUtNS42IDUtMy40IDAtNS42LTEuOS01LjYtNXYtMy43YzAtMy4xIDIuMS01IDUuNi01IDMuNSAwIDUuNiAxLjkgNS42IDV6bS0zLjUgMGMwLTEuMi0uNy0yLTItMnMtMiAuNy0yIDJWMzFjMCAxLjIuNyAxLjkgMiAxLjlzMi0uNyAyLTEuOXYtMy43em0tMjIuMy0xLjdjMCAzLjItMi40IDUuNC01LjYgNS40LS44IDAtMS41LS4xLTIuMi0uNHY0LjVjMCAuMy0uMy42LS42LjZoLTIuM2MtLjMgMC0uNi0uMy0uNi0uNlYxOS4yYzAtLjQuMy0uNy42LS44IDEuNS0uNSAzLS44IDQuNi0uOCAzLjYgMCA2LjEgMi4yIDYuMSA1LjZ2Mi40ek01MS43IDIzYzAtMS42LTEuMS0yLjQtMi42LTIuNC0uOSAwLTEuNS4zLTEuNS4zdjYuNmMuNi4zLjkuNCAxLjYuNCAxLjUgMCAyLjYtLjkgMi42LTIuNFYyM3ptNjguMiAyLjZjMCAzLjItMi40IDUuNC01LjYgNS40LS44IDAtMS41LS4xLTIuMi0uNHY0LjVjMCAuMy0uMy42LS42LjZoLTIuM2MtLjMgMC0uNi0uMy0uNi0uNlYxOS4yYzAtLjQuMy0uNy42LS44IDEuNS0uNSAzLS44IDQuNi0uOCAzLjYgMCA2LjEgMi4yIDYuMSA1LjZ2Mi40em0tMy42LTIuNmMwLTEuNi0xLjEtMi40LTIuNi0yLjQtLjkgMC0xLjUuMy0xLjUuM3Y2LjZjLjYuMy45LjQgMS42LjQgMS41IDAgMi42LS45IDIuNi0yLjRWMjN6Ii8+PHBhdGggZD0iTTI2IDE5LjNjMC0uNy0uNi0xLjMtMS4zLTEuM2gtMi40bC01LjUtNi4zYy0uNS0uNi0xLjMtLjgtMi4xLS42bC0xLjkuNmMtLjMuMS0uNC41LS4yLjdsNiA1LjdIOS41Yy0uMyAwLS41LjItLjUuNXYxYzAgLjcuNiAxLjMgMS4zIDEuM2gxLjR2NC44YzAgMy42IDEuOSA1LjcgNS4xIDUuNyAxIDAgMS44LS4xIDIuOC0uNXYzLjJjMCAuOS43IDEuNiAxLjYgMS42aDEuNGMuMyAwIC42LS4zLjYtLjZWMjAuOGgyLjNjLjMgMCAuNS0uMi41LS41di0xem0tNi40IDguNmMtLjYuMy0xLjQuNC0yIC40LTEuNiAwLTIuNC0uOC0yLjQtMi42di00LjhoNC40djd6IiBmaWxsPSIjZmZmIi8+PC9zdmc+" alt="">
  <h1 class="m-5 font-bold text-xl">Business Solutions</h1>
  <h1 class="m-5 font-bold text-xl">Insurance</h1>
  <h1 class="m-5 font-bold text-xl">Investments</h1>
  <h1 class="m-5 font-bold text-xl">General</h1>
  <h1 class="m-5 font-bold text-xl">Legal</h1>
  <h1 class="m-5 font-bold text-xl">Certification</h1>
</div>

<div class="p-10 flex items-start gap-10">
  <img class="h-16" src="data:image/svg+xml;base64,PHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSJMYXllcl8yIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHg9IjAiIHk9IjAiIHZpZXdCb3g9IjAgMCAxMzIgNDgiIHhtbDpzcGFjZT0icHJlc2VydmUiPjxzdHlsZT4uc3Qwe2ZpbGw6IzVmMjU5Zn08L3N0eWxlPjxjaXJjbGUgdHJhbnNmb3JtPSJyb3RhdGUoLTc2LjcxNCAxNy44NyAyNC4wMDEpIiBjbGFzcz0ic3QwIiBjeD0iMTcuOSIgY3k9IjI0IiByPSIxNy45Ii8+PHBhdGggY2xhc3M9InN0MCIgZD0iTTkwLjUgMzQuMnYtNi41YzAtMS42LS42LTIuNC0yLjEtMi40LS42IDAtMS4zLjEtMS43LjJWMzVjMCAuMy0uMy42LS42LjZoLTIuM2MtLjMgMC0uNi0uMy0uNi0uNlYyMy45YzAtLjQuMy0uNy42LS44IDEuNS0uNSAzLS44IDQuNi0uOCAzLjYgMCA1LjYgMS45IDUuNiA1LjR2Ny40YzAgLjMtLjMuNi0uNi42SDkyYy0uOSAwLTEuNS0uNy0xLjUtMS41em05LTMuOWwtLjEuOWMwIDEuMi44IDEuOSAyLjEgMS45IDEgMCAxLjktLjMgMi45LS44LjEgMCAuMi0uMS4zLS4xLjIgMCAuMy4xLjQuMi4xLjEuMy40LjMuNC4yLjMuNC43LjQgMSAwIC41LS4zIDEtLjcgMS4yLTEuMS42LTIuNC45LTMuOC45LTEuNiAwLTIuOS0uNC0zLjktMS4yLTEtLjktMS42LTIuMS0xLjYtMy42di0zLjljMC0zLjEgMi01IDUuNC01IDMuMyAwIDUuMiAxLjggNS4yIDV2Mi40YzAgLjMtLjMuNi0uNi42aC02LjN6bS0uMS0yLjJIMTAzLjJ2LTFjMC0xLjItLjctMi0xLjktMnMtMS45LjctMS45IDJ2MXptMjUuNSAyLjJsLS4xLjljMCAxLjIuOCAxLjkgMi4xIDEuOSAxIDAgMS45LS4zIDIuOS0uOC4xIDAgLjItLjEuMy0uMS4yIDAgLjMuMS40LjIuMS4xLjMuNC4zLjQuMi4zLjQuNy40IDEgMCAuNS0uMyAxLS43IDEuMi0xLjEuNi0yLjQuOS0zLjguOS0xLjYgMC0yLjktLjQtMy45LTEuMi0xLS45LTEuNi0yLjEtMS42LTMuNnYtMy45YzAtMy4xIDItNSA1LjQtNSAzLjMgMCA1LjIgMS44IDUuMiA1djIuNGMwIC4zLS4zLjYtLjYuNmgtNi4zem0tLjEtMi4ySDEyOC42di0xYzAtMS4yLS43LTItMS45LTJzLTEuOS43LTEuOSAydjF6TTY2IDM1LjdoMS40Yy4zIDAgLjYtLjMuNi0uNnYtNy40YzAtMy40LTEuOC01LjQtNC44LTUuNC0uOSAwLTEuOS4yLTIuNS40VjE5YzAtLjgtLjctMS41LTEuNS0xLjVoLTEuNGMtLjMgMC0uNi4zLS42LjZ2MTdjMCAuMy4zLjYuNi42aDIuM2MuMyAwIC42LS4zLjYtLjZ2LTkuNGMuNS0uMiAxLjItLjMgMS43LS4zIDEuNSAwIDIuMS43IDIuMSAyLjR2Ni41Yy4xLjcuNyAxLjQgMS41IDEuNHptMTUuMS04LjRWMzFjMCAzLjEtMi4xIDUtNS42IDUtMy40IDAtNS42LTEuOS01LjYtNXYtMy43YzAtMy4xIDIuMS01IDUuNi01IDMuNSAwIDUuNiAxLjkgNS42IDV6bS0zLjUgMGMwLTEuMi0uNy0yLTItMnMtMiAuNy0yIDJWMzFjMCAxLjIuNyAxLjkgMiAxLjlzMi0uNyAyLTEuOXYtMy43em0tMjIuMy0xLjdjMCAzLjItMi40IDUuNC01LjYgNS40LS44IDAtMS41LS4xLTIuMi0uNHY0LjVjMCAuMy0uMy42LS42LjZoLTIuM2MtLjMgMC0uNi0uMy0uNi0uNlYxOS4yYzAtLjQuMy0uNy42LS44IDEuNS0uNSAzLS44IDQuNi0uOCAzLjYgMCA2LjEgMi4yIDYuMSA1LjZ2Mi40ek01MS43IDIzYzAtMS42LTEuMS0yLjQtMi42LTIuNC0uOSAwLTEuNS4zLTEuNS4zdjYuNmMuNi4zLjkuNCAxLjYuNCAxLjUgMCAyLjYtLjkgMi42LTIuNFYyM3ptNjguMiAyLjZjMCAzLjItMi40IDUuNC01LjYgNS40LS44IDAtMS41LS4xLTIuMi0uNHY0LjVjMCAuMy0uMy42LS42LjZoLTIuM2MtLjMgMC0uNi0uMy0uNi0uNlYxOS4yYzAtLjQuMy0uNy42LS44IDEuNS0uNSAzLS44IDQuNi0uOCAzLjYgMCA2LjEgMi4yIDYuMSA1LjZ2Mi40em0tMy42LTIuNmMwLTEuNi0xLjEtMi40LTIuNi0yLjQtLjkgMC0xLjUuMy0xLjUuM3Y2LjZjLjYuMy45LjQgMS42LjQgMS41IDAgMi42LS45IDIuNi0yLjRWMjN6Ii8+PHBhdGggZD0iTTI2IDE5LjNjMC0uNy0uNi0xLjMtMS4zLTEuM2gtMi40bC01LjUtNi4zYy0uNS0uNi0xLjMtLjgtMi4xLS42bC0xLjkuNmMtLjMuMS0uNC41LS4yLjdsNiA1LjdIOS41Yy0uMyAwLS41LjItLjUuNXYxYzAgLjcuNiAxLjMgMS4zIDEuM2gxLjR2NC44YzAgMy42IDEuOSA1LjcgNS4xIDUuNyAxIDAgMS44LS4xIDIuOC0uNXYzLjJjMCAuOS43IDEuNiAxLjYgMS42aDEuNGMuMyAwIC42LS4zLjYtLjZWMjAuOGgyLjNjLjMgMCAuNS0uMi41LS41di0xem0tNi40IDguNmMtLjYuMy0xLjQuNC0yIC40LTEuNiAwLTIuNC0uOC0yLjQtMi42di00LjhoNC40djd6IiBmaWxsPSIjZmZmIi8+PC9zdmc+" alt="">
  <div class="flex flex-col gap-5">
    <h1 class="font-bold text-xl hover:text-purple-600">Insurance</h1>
    <ul class="text-sm flex flex-col gap-3 ">
      <li class=" hover:text-purple-600">Payment Gateway</li>
      <li class=" hover:text-purple-600">Guardian by PhonePe</li>
      <li class=" hover:text-purple-600">Express Checkout</li>
      <li class=" hover:text-purple-600">PhonePe Switch</li>
      <li class=" hover:text-purple-600">Offline Merchant</li>
      <li class=" hover:text-purple-600">Advertise on PhonePe</li>
      <li class=" hover:text-purple-600">SmartSpeaker</li>
      <li class=" hover:text-purple-600">Phonepe Lending</li>
      <li class=" hover:text-purple-600">POS Machine</li>
    </ul>
  </div>
  <div class="flex flex-col gap-5">
    <h1 class="font-bold text-xl hover:text-purple-600">Investments</h1>
    <ul class="text-sm flex flex-col gap-3 ">
      <li class=" hover:text-purple-600">Payment Gateway</li>
      <li class=" hover:text-purple-600">Guardian by PhonePe</li>
      <li class=" hover:text-purple-600">Express Checkout</li>
      <li class=" hover:text-purple-600">PhonePe Switch</li>
      <li class=" hover:text-purple-600">Offline Merchant</li>
      <li class=" hover:text-purple-600">Advertise on PhonePe</li>
      <li class=" hover:text-purple-600">SmartSpeaker</li>
      <li class=" hover:text-purple-600">Phonepe Lending</li>
      <li class=" hover:text-purple-600">POS Machine</li>
    </ul>
  </div>
  <div class="flex flex-col gap-5">
    <h1 class="font-bold text-xl hover:text-purple-600">General</h1>
    <ul class="text-sm flex flex-col gap-3 ">
      <li class=" hover:text-purple-600">Payment Gateway</li>
      <li class=" hover:text-purple-600">Guardian by PhonePe</li>
      <li class=" hover:text-purple-600">Express Checkout</li>
      <li class=" hover:text-purple-600">PhonePe Switch</li>
      <li class=" hover:text-purple-600">Offline Merchant</li>
      <li class=" hover:text-purple-600">Advertise on PhonePe</li>
      <li class=" hover:text-purple-600">SmartSpeaker</li>
      <li class=" hover:text-purple-600">Phonepe Lending</li>
      <li class=" hover:text-purple-600">POS Machine</li>
    </ul>
  </div>
  <div class="flex flex-col gap-5">
    <h1 class="font-bold text-xl hover:text-purple-600">Legal</h1>
    <ul class="text-sm flex flex-col gap-3 ">
      <li class=" hover:text-purple-600">Payment Gateway</li>
      <li class=" hover:text-purple-600">Guardian by PhonePe</li>
      <li class=" hover:text-purple-600">Express Checkout</li>
      <li class=" hover:text-purple-600">PhonePe Switch</li>
      <li class=" hover:text-purple-600">Offline Merchant</li>
      <li class=" hover:text-purple-600">Advertise on PhonePe</li>
      <li class=" hover:text-purple-600">SmartSpeaker</li>
      <li class=" hover:text-purple-600">Phonepe Lending</li>
      <li class=" hover:text-purple-600">POS Machine</li>
    </ul>
  </div>
  <div class="flex flex-col gap-5">
    <h1 class="font-bold text-xl hover:text-purple-600">Business Solutions</h1>
    <ul class="text-sm flex flex-col gap-3 ">
      <li class=" hover:text-purple-600">Payment Gateway</li>
      <li class=" hover:text-purple-600">Guardian by PhonePe</li>
      <li class=" hover:text-purple-600">Express Checkout</li>
      <li class=" hover:text-purple-600">PhonePe Switch</li>
      <li class=" hover:text-purple-600">Offline Merchant</li>
      <li class=" hover:text-purple-600">Advertise on PhonePe</li>
      <li class=" hover:text-purple-600">SmartSpeaker</li>
      <li class=" hover:text-purple-600">Phonepe Lending</li>
      <li class=" hover:text-purple-600">POS Machine</li>
    </ul>
  </div>
  <div class="flex flex-col gap-5">
    <h1 class="font-bold text-xl hover:text-purple-600">Certifications</h1>
    <img src="https://www.phonepe.com/webstatic/7083/static/sisa-f4b48e5a5d0f5862515676359b94c75a.png" alt="">
    <h1 class="font-bold text-xl hover:text-purple-600">See All Apps</h1>
    <h1 class=" bg-purple-500 rounded-xl mr-auto p-5 text-white">DOWNLOAD NOW</h1>
  </div>

</div>






</template>
<script setup>

</script>

<style scoped>
.body{
  max-width: 1440px;
}

</style>