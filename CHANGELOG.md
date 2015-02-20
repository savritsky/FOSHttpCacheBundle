Changelog
=========

1.3.0
-----

* **2015-02-20** Configured/annotated tags on subrequests (twig `render(controller())`)
  are no longer ignored. Additionally, it is now possible to add tags from code before
  the response has been created.

1.2.0
-----

* **2014-12-05** Refactored the Symfony built-in HttpCache support to be extensible.
  FOS\HttpCacheBundle\HttpCache is deprecated in favor of EventDispatchingHttpCache.

  BC break: If you overwrite cleanupForwardRequest in your cache kernel, you need to
  extend FOS\HttpCache\SymfonyCache\UserContextSubscriber and move that logic to the
  method cleanupHashLookupRequest in there.

1.1.0
-----

* **2014-10-14** Allow cache headers overwrite.
* **2014-10-29** Added support for the user context lookup with Symfony built-in
  reverse proxy, aka `HttpCache`.

1.0.0
-----

Initial release. To migrate from other Symfony2 cache bundles, see
[LiipCacheControlBundle](https://github.com/liip/LiipCacheControlBundle) or
[DriebitHttpCacheBundle](https://github.com/driebit/DriebitHttpCacheBundle).
