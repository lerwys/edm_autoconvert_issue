EDM autoconvert issue
=====================

This example .edl screen has 6 buttons associated with
a different longout PV bit named "longoutPV".

When autoconverting the .edl to .bob with the following
command:

```bash
phoebus -main org.csstudio.display.converter.edm.Converter \
    -colors colors.list \
    -output . \
    test_multi_button.edl
```

I get:

```bash
lrusso@lrussoPC:~/repos/test_edm$ phoebus -main org.csstudio.display.converter.edm.Converter -colors colors.list -output . test_multi_button.edl
2023-09-28 15:57:52 CONFIG [org.phoebus.product.Launcher] Loading settings from /opt/phoebus/phoebus-4.7.3-SNAPSHOT/settings.ini
2023-09-28 15:57:52 INFO [org.csstudio.display.converter.edm] Reading colors.list
2023-09-28 15:57:52 INFO [org.csstudio.display.converter.edm] Convert test_multi_button.edl -> ./test_multi_button.bob
```

But the resulting .bob shows all the converted buttons associated
with the same bit ("0", in this case).

Phoebus version used:

```bash
Phoebus 4.7.3-SNAPSHOT
build "master 2023-07-25 14:51"
```
