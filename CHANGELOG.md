# FetchImage 0.x

## FetchImage 0.6.0

*April 17, 2021*

- Added `ScrollViewPrefetcher` which can be accessed via a `PrefetchImageModel` object. This helps prefetch images when using SwiftUI collections.
- Updated to Nuke 9.5
- Updated to Firebase 7.10
- Added background loading for Firebase URLs
- `@Publishable` updates are now all on the main thread


## FetchImage 0.5.0

*March 16, 2021*

- The Firebase `load` call now provides a URL once cached.

## FetchImage 0.4.0

*March 03, 2021*

- **Internal Change** `ImageRequest` objects are now optional and may not be immediately fulfilled when initializing a `FetchImage` instance. This allows expansion of the API for additional changes and improvements.
- Google Firebase support. Using the new convenience initializer to create a `FetchImage` instance with a Firestore `StorageReference` instead of directly from a URL. Optionally, supply any cached URL content when using this initializer to decrease Firestore roundtrips.
- Fixed and expanded in-line documentation.

## FetchImage 0.3.0

*December 26, 2020*

- **Breaking Change** `FetchImage` no longer starts the request in the initializer, you must call `fetch()`.
- Add `reset()` method which clears the entire `FetchImage` state including the downloaded image. This is crucial for long lists where you don't want `FetchImage` instances to retain images which are off screen.

## FetchImage 0.2.1

*May 23, 2020*

- Fix build error – [#3](https://github.com/kean/FetchImage/pull/3) by [Yu Tawata](https://github.com/yuta24)

## FetchImage 0.2.0

*May 20, 2020*

- Update to Nuke 9

## FetchImage 0.1.0

*March 19, 2020*

- Initial release. See an [introductory post](https://kean.github.io/post/introducing-fetch-image) for more information.
