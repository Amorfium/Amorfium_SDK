# Amorfium SDK (Alpha Development Version)

This repository contains the source code and documentation for the Amorfium SDK, a robust and adaptable toolkit created to simplify the creation of gaming utilities on the Windows platform.

The primary objective of the project is to offer a comprehensive set of features that enables a gaming utility developer to meet all their requirements. In addition, the project goal is to offer its full capabilities on "bare hardware", without relying on CRT (C Run-Time) and utilizing the basic functionality of STL (Standard Template Library). It should be emphasized that CRT can be integrated with our library after some manipulation, if needed. Our SDK is intended solely for the Windows OS and is meticulously designed to provide developers with ample opportunity to develop additional game features. At this stage of our project, our focus is on supporting x64 applications and ensuring compatibility with Windows 11. We plan to include support for x86 applications in the future to expand coverage.

## Table of Contents

- [Disclaimer](#disclaimer)
- [Compatibility](#compatibility)
- [Usage](#usage)
- [Feadback and Collaboration](#feadback-and-collaboration)
- [Credits](#credits)
- [License](#license)
- [Additional Information](#additional-information)

## Disclaimer

The Amorfium SDK is intended to be used solely for educational purposes and for legitimate development purposes. Its tools and features are designed to assist game developers in creating various game add-ons. Any misuse, including the use of our project for game manipulation, hacking, or obtaining unfair advantages in online games, is strictly prohibited and may result in legal action.

We disclaim any responsibility for the misuse of the Amorfium SDK that violates applicable laws, regulations, or ethical standards.

Our project offers valuable insights into programming and software development but it is crucial to understand that it was created for learning and exploration purposes. The Amorfium Team provides the project "as-is." If misuse occurs, individuals responsible for misusing the project, not the Amorfium Team, are liable for any complaints or issues.

We encourage responsible and ethical use of the Amorfium SDK and compliance with all applicable laws and regulations. If you have any inquiries regarding our project's acceptable use, please do not hesitate to contact us for further clarification.

Please note that our project is solely intended as an educational example and we do not endorse or support any illegal activities or the abuse of the tools and information it provides.

## Compatibility

Our goal is to cover all versions of Windows from version 10 onwards. However, the full functionality of our SDK has been tested on these versions:
- Windows 10 (x64) - 21H2 (Build 19041.1288)
- Windows 10 (x64) - 22H2 (Build 19045.2965)
- Windows 11 (x64) - 21H2 (Build 22000.194)
- Windows 11 (x64) - 22H2 (Build 22621.382)

## Usage

Amorfium SDK is an advanced library designed to be integrated into your projects as a static library, compiled along with your project. The library is distributed as a CMake-based project, making it easy to integrate into your project. The library is divided into modules, each responsible for a specific area of functionality.

How to properly integrate a library with CMake:

1. Clone the repository to your local machine.

2. Create a new folder in the root directory of your project and name it "amorfium_sdk".

3. Copy the contents of the "amorfium_sdk" folder from the repository to the folder you created in the previous step.

4. Add the following lines to your CMakeLists.txt file:
```cmake
add_subdirectory(amorfium_sdk)
target_link_libraries(<your_project_name> amorfium::sdk)
```

5. Add the following line to your main.cpp file:
```cpp
#include "<your_project_source_directory>/amorfium_sdk/src/core/core.hxx"
```

6. Build your project.

## Feadback and Collaboration

We value feedback from our users and encourage you to share your thoughts, suggestions and ideas for further development. Collaboration is at the heart of our project's growth, and we invite you to join us in shaping the future of the Amorfium SDK. Before you contribute, please read the license agreement to understand the scope of our project.

## Credits

Our project was made possible by the collaborative contributions of several individuals. We would like to give special thanks to the following:

- The Amorfium team (individual development of [mxrz](https://github.com/Aleksandr-Strashevskiy))
- [LCShasH](https://github.com/LCShasH) (for moral support and inspiration)

If you've contributed to the project and would like to be listed here, please submit a [pull request](https://github.com/Amorfium/amorfium_sdk/pulls) with your information added to the credits.

## License

> Copyright © 2023-present Amorfium Team.

This project is licensed under the terms of the [MIT License with Amorfium Team Exception](LICENSE).

## Additional Information

There are compilation and link flags set in the project (see [CMakeLists](cmakelists.txt#L74)), please, if you are not very familiar with how they work, do not touch them, or override them at your own risk.

Most of the necessary documentation is not yet done and documented, but we are working on it (you can always help us if you want to).