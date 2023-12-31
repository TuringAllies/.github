<!-- Improved compatibility of back to top link: See: https://github.com/TuringAllies/turingAllies/pull/73 -->

<a name="readme-top"></a>

<!--
*** Thanks for checking out the TuringAllies Repo. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">

  <h1 align="center">Turing Allies</h1>

  <p align="center">
    An Open Source project for students to use <i>or</i> contribute to
    <br />
    <br />
    <img src="app/assets/images/gears.jpg" alt="logo stuff" style="width:500px;height:auto" >
    <br />
    <a href=""><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="">View Demo</a>
    ·
    <a href="https://github.com/TuringAllies/turingAllies/issues/new?assignees=&labels=&projects=&template=bug_report.md&title=">Report Bug</a>
    ·
    <a href="https://github.com/TuringAllies/turingAllies/issues/new?assignees=&labels=&projects=&template=feature_request.md&title=">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<div style="width:200px;margin:0 auto;padding:1rem;">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#debugging">Debugging</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</div>

<!-- ABOUT THE PROJECT -->

## About The Project

This is an Open Source project created by Turing students

It started with a simple idea:

> create a platform/website or service for Students to see companies that have interviewed or hired Turing students

While the job hunt can be long and difficult, part of the price of admission to Turing is access to it's existing, never-ending network of alumni.

Just like we supported each other through the program itself, I'd like to believe we continue to support each other professionally through the duration of our careers.

At the same time, it's also important to continue to code, build and contribute to Open Source projects.

The amount of complex logic I've ever needed for my day to day job is null. The most complex logic I've ever really had to use is "if this, do this, else, do that". Spending hours doing code challenges is, IMO, less beneficial than building.

Contributing to an Open Source project can be intimidating, especially when you've never done it before.

This project, no matter how inactive, is 100% built by Turing grads and students. You're never out of place by creating a PR for this project. There are safeguards in place that prevent you from ruining anything.

If you'd like to improve, work on, or suggest something for this project while you also search for a job, that's awesome!

Contribute one small thing (whatever you suggest will most likely be merged in) and then you can put it on your resume!

Simple as that.

Obviously contributing more would look better to an employer, but hey, do what you can.

Or just use the website. That's fine too.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

-   [![Ruby][ruby.com]][ruby-url]
-   [![Rails][rails.com]][rails-url]
-   [![Rspec][rspec.com]][rspec-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- GETTING STARTED -->

## Getting Started

### Prerequisites

- ruby v3.1.4
- rails v7
- postgresql

### Installation

1. Clone the repo like you normally would, onto your local machine

    ```bash
    git clone git@github.com:TuringAllies/turingAllies.git
    ```
2. CD into the project

   ```bash
   cd turingAllies/
   ```
3. Install packages by running:
    ```bash
    # does the same thing as `bundle install`
    bundle
    ```
4. Setup the database

    ```bash
    rails db:create
    ```

5. Run the migrations
    ```bash
    rails db:migrate
    ```
6. Precompile the assets (this might not be necessary; see [this doc](https://github.com/TuringAllies/turingAllies/blob/main/docs/issues_with_assets.md) for more details)
    ```bash
    bundle exec rake assets:precompile
    ```

7. load employer data to be displayed by running the following command
    ```bash
    bundle exec rake csv_load:populate_employers
    ```

8. Copy the file title `application.sample.yml` and rename it `application.yml`

   ```bash
   cp config/application.sample.yml config/application.yml
   ```

9. Add the `CLIENT_ID` and `CLIENT_SECRET` to `application.yml`

  - This step is necessary to enable Omniauth with Github locally
  - in the Github repo for the turingAllies [ORGANIZATION](https://github.com/TuringAllies) go to [Settings](https://github.com/organizations/TuringAllies/settings/profile)
  - click on "Developer Settings"
  - select "OAuth apps"
  - click "turingAllies"
  - copy the `CLIENT_ID` and paste it in your `application.yml` file
  - do the same with the `CLIENT_SECRET`
  - If you run into any issues with this, DM me on Turing's Slack

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->

## Usage

To spin up this project, run the following command from the command line:

```
bin/dev
```

navigation to `localhost:3000` and see the website there


<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- DEBUGGING EXAMPLES -->

## Debugging

To debug this project, DO NOT start the app with `bin/dev`.

Instead, start the app with the typical

```
rails server
```

Then add a `debugger` anywhere in the code to hit the binding.

To learn more about the default debugger gem in Rails 7 apps, head over to [the debug gem](https://github.com/ruby/debug)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
2. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
3. Pull the `main` branch into your feature branch (`git pull origin main`)
4. Resolve any merge conflicts locally
5. Push to the Branch (`git push origin feature/AmazingFeature`)
6. Open a Pull Request by completing the PR on github

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->

## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->

## Contact

Michael Marchand - MichaelDavidMarchand@gmail.com

Project Link: [https://github.com/TuringAllies/turingAllies](https://github.com/TuringAllies/turingAllies)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->

## Acknowledgments

Use this space to list resources you find helpful and would like to give credit to. I've included a few of my favorites to kick things off!

-   [Choose an Open Source License](https://choosealicense.com)
-   [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
-   [Img Shields](https://shields.io)
-   [GitHub Pages](https://pages.github.com)
-   [Rubocop](https://rubocop.org/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/TuringAllies/turingAllies.svg?style=for-the-badge
[contributors-url]: https://github.com/TuringAllies/turingAllies/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/TuringAllies/turingAllies.svg?style=for-the-badge
[forks-url]: https://github.com/TuringAllies/turingAllies/network/members
[stars-shield]: https://img.shields.io/github/stars/TuringAllies/turingAllies?style=for-the-badge
[stars-url]: https://github.com/TuringAllies/turingAllies/stargazers
[issues-shield]: https://img.shields.io/github/issues/TuringAllies/turingAllies?style=for-the-badge
[issues-url]: https://github.com/TuringAllies/turingAllies/issues
[license-shield]: https://img.shields.io/github/license/TuringAllies/turingAllies.svg?style=for-the-badge
[license-url]: https://github.com/TuringAllies/turingAllies/blob/master/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/mmarchand1/
[product-screenshot]: images/screenshot.png
[bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[bootstrap-url]: https://getbootstrap.com
[ruby.com]: https://img.shields.io/badge/ruby-v3.1.4-red
[ruby-url]: https://ruby-doc.org/core-2.7.2/
[rails.com]: https://img.shields.io/badge/rails-v7.1.2-red
[rails-url]: https://api.rubyonrails.org/
[rspec.com]: https://img.shields.io/badge/rspec-v3.12-success
[rspec-url]: https://rspec.info/documentation/
