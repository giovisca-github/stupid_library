## Project_NAME
<div class="title_screenshot">

![immagine per fare figura](docs/img/Untitled.png)

</div>

[Website Documentation](https://giovisca-github.github.io/stupid_library/)


# jobs:
#   build:
#     name: Build and publish documentation
#     runs-on: ubuntu-latest
#     steps:
#     - uses: actions/checkout@v2
#     - uses: actions/setup-python@v2
#     - name: Install Docs
#       run: |
#         sudo apt-get install doxygen
#         pip install jinja2 Pygments
#     - name: prepare
#       run: |
#         make prepare
#     - name: configure
#       run: |
#         cmake -H. -Bbuild -G "Unix Makefiles" -DCMAKE_BUILD_TYPE="Debug"
#     - name: building
#       run: |
#         cmake --build build --config Debug --target docs -j4

    # - name: Generate Documentation
    #   uses: mattnotmitt/doxygen-action@edge
    #   with:
    #       working-directory: 'docs'
    # - name: Publish generated content to GitHub Pages
      # uses: tsunematsu21/actions-publish-gh-pages@v1.0.2
      # with:
      #    dir: ./docs/html
      #    branch: gh-pages
      #    token: ${{ secrets.ACCESS_TOKEN }}

    # - name: Deploy to GitHub Pages
    #   uses: Cecilapp/GitHub-Pages-deploy@v3
    #   env:
    #     GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
    #   with:
    #     build_dir: ./docs/html

# jobs:
#   deploy:
#     runs-on: ubuntu-20.04
#     steps:
#       - name: Checkout repository
#         uses: actions/checkout@v2
#         with:
#           fetch-depth: 0
#       # - name: set version
#       #   run: echo "PROJECT_NUMBER = `git describe --tags`" >> Doxyfile
#       - name: Generate Documentation
#         uses: mattnotmitt/doxygen-action@edge
#         with:
#           working-directory: 'docs/'
#       # - name: Publish generated content to GitHub Pages
#       #   uses: tsunematsu21/actions-publish-gh-pages@v1.0.2
#       #   with:
#       #     dir: docs/html
#       #     branch: gh-pages
#       #     token: ${{ secrets.GITHUB_TOKEN  }}