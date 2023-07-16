---
title: Release {{ env.VERSION }}
labels: RELEASE
---

Author: {{ tools.context.actor }}
Version: {{ env.VERSION }}
Date: {{ date | date('dddd, MMMM Do') }}

Published: {{ env.URL }}

Reports:

- {{ env.REPORT1 }}
- {{ env.REPORT2 }}

### Changelog

{{ env.CHANGELOG }}
