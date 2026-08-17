# Lab 17 Benchmark Report

- Implementation: `student`
- Kind: `practice`
- Cases: **11**
- Passed: **2/11**
- Evidence hit rate: **18.2%**
- Average retrieval latency: **392.9 ms**
- Average token reduction vs full source context: **81.8%**

| Case | Layer | Pass | Latency ms | Retrieved tokens | Token reduction | Missing / Error |
| --- | --- | --- | ---: | ---: | ---: | --- |
| E01 | short_term | PASS | 0.1 | 133 | 0.0% |  |
| E06 | semantic | FAIL | 1188.9 | 0 | 100.0% | ApiError: headers: {'date': 'Mon, 17 Aug 2026 16:57:22 GMT', 'content-type': 'text/plain; charset=utf-8', 'content-length': '13', 'connection': 'keep-alive', 'vary': 'Origin', 'x-content-type-options': 'nosniff', 'strict-transport-security': 'max-age=2592000', 'cf-cache-status': 'DYNAMIC', 'server': 'cloudflare', 'cf-ray': 'a2ca37aa1c6fe2ff-HKG'}, status_code: 401, body: unauthorized
 |
| E09 | long_term | FAIL | 866.0 | 0 | 100.0% | ApiError: headers: {'date': 'Mon, 17 Aug 2026 16:57:23 GMT', 'content-type': 'text/plain; charset=utf-8', 'content-length': '13', 'connection': 'keep-alive', 'content-security-policy-report-only': "script-src 'unsafe-inline' 'unsafe-eval'; report-uri https://csp-reporting.cloudflare.com/cdn-cgi/script_monitor/report?m=PZbll1hi2a91X38PPgPdQ1mMIEFUySvu51VTYOnourU-1786985843.1305618-1.0.1.1-Gkpu_hQD_1XcWrfCFWD_Com2YpsXeDa0Id4AnGlXSCUKSVYsruKhWnzxJOHeG1Fp3E4P4vuIsMsg9wrQ3PU7Td7I2.00ZHGBXt1SsL6MQhNQepMQSMVZYmkctvl09CinUSD.q37fp0aune9IdJHZwuc5nf84UhRe72ibu5IFSIg; report-to cf-csp-endpoint", 'vary': 'Origin', 'x-content-type-options': 'nosniff', 'strict-transport-security': 'max-age=2592000', 'reporting-endpoints': 'cf-csp-endpoint="https://csp-reporting.cloudflare.com/cdn-cgi/script_monitor/report?m=PZbll1hi2a91X38PPgPdQ1mMIEFUySvu51VTYOnourU-1786985843.1305618-1.0.1.1-Gkpu_hQD_1XcWrfCFWD_Com2YpsXeDa0Id4AnGlXSCUKSVYsruKhWnzxJOHeG1Fp3E4P4vuIsMsg9wrQ3PU7Td7I2.00ZHGBXt1SsL6MQhNQepMQSMVZYmkctvl09CinUSD.q37fp0aune9IdJHZwuc5nf84UhRe72ibu5IFSIg"', 'cf-cache-status': 'DYNAMIC', 'report-to': '{"group":"cf-csp-endpoint","max_age":86400,"endpoints":[{"url":"https://csp-reporting.cloudflare.com/cdn-cgi/script_monitor/report?m=PZbll1hi2a91X38PPgPdQ1mMIEFUySvu51VTYOnourU-1786985843.1305618-1.0.1.1-Gkpu_hQD_1XcWrfCFWD_Com2YpsXeDa0Id4AnGlXSCUKSVYsruKhWnzxJOHeG1Fp3E4P4vuIsMsg9wrQ3PU7Td7I2.00ZHGBXt1SsL6MQhNQepMQSMVZYmkctvl09CinUSD.q37fp0aune9IdJHZwuc5nf84UhRe72ibu5IFSIg"}]}', 'server': 'cloudflare', 'cf-ray': 'a2ca37af8a1be2ff-HKG'}, status_code: 401, body: unauthorized
 |
| E10 | short_term | PASS | 0.3 | 195 | 0.0% |  |
| E02 | long_term | FAIL | 454.4 | 0 | 100.0% | ApiError: headers: {'date': 'Mon, 17 Aug 2026 16:57:23 GMT', 'content-type': 'text/plain; charset=utf-8', 'content-length': '13', 'connection': 'keep-alive', 'vary': 'Origin', 'x-content-type-options': 'nosniff', 'strict-transport-security': 'max-age=2592000', 'cf-cache-status': 'DYNAMIC', 'server': 'cloudflare', 'cf-ray': 'a2ca37b268b6e2ff-HKG'}, status_code: 401, body: unauthorized
 |
| E03 | long_term | FAIL | 358.1 | 0 | 100.0% | ApiError: headers: {'date': 'Mon, 17 Aug 2026 16:57:24 GMT', 'content-type': 'text/plain; charset=utf-8', 'content-length': '13', 'connection': 'keep-alive', 'vary': 'Origin', 'x-content-type-options': 'nosniff', 'strict-transport-security': 'max-age=2592000', 'cf-cache-status': 'DYNAMIC', 'server': 'cloudflare', 'cf-ray': 'a2ca37b4be49e2ff-HKG'}, status_code: 401, body: unauthorized
 |
| E04 | episodic | FAIL | 183.4 | 0 | 100.0% | ApiError: headers: {'date': 'Mon, 17 Aug 2026 16:57:24 GMT', 'content-type': 'text/plain; charset=utf-8', 'content-length': '13', 'connection': 'keep-alive', 'vary': 'Origin', 'x-content-type-options': 'nosniff', 'strict-transport-security': 'max-age=2592000', 'cf-cache-status': 'DYNAMIC', 'server': 'cloudflare', 'cf-ray': 'a2ca37b5e966e2ff-HKG'}, status_code: 401, body: unauthorized
 |
| E05 | episodic | FAIL | 187.5 | 0 | 100.0% | ApiError: headers: {'date': 'Mon, 17 Aug 2026 16:57:24 GMT', 'content-type': 'text/plain; charset=utf-8', 'content-length': '13', 'connection': 'keep-alive', 'vary': 'Origin', 'x-content-type-options': 'nosniff', 'strict-transport-security': 'max-age=2592000', 'cf-cache-status': 'DYNAMIC', 'server': 'cloudflare', 'cf-ray': 'a2ca37b71c66e2ff-HKG'}, status_code: 401, body: unauthorized
 |
| E07 | mixed | FAIL | 357.1 | 0 | 100.0% | ApiError: headers: {'date': 'Mon, 17 Aug 2026 16:57:24 GMT', 'content-type': 'text/plain; charset=utf-8', 'content-length': '13', 'connection': 'keep-alive', 'vary': 'Origin', 'x-content-type-options': 'nosniff', 'strict-transport-security': 'max-age=2592000', 'cf-cache-status': 'DYNAMIC', 'server': 'cloudflare', 'cf-ray': 'a2ca37b969a4e2ff-HKG'}, status_code: 401, body: unauthorized
 |
| E11 | semantic | FAIL | 359.4 | 0 | 100.0% | ApiError: headers: {'date': 'Mon, 17 Aug 2026 16:57:25 GMT', 'content-type': 'text/plain; charset=utf-8', 'content-length': '13', 'connection': 'keep-alive', 'vary': 'Origin', 'x-content-type-options': 'nosniff', 'strict-transport-security': 'max-age=2592000', 'cf-cache-status': 'DYNAMIC', 'server': 'cloudflare', 'cf-ray': 'a2ca37bbaeb1e2ff-HKG'}, status_code: 401, body: unauthorized
 |
| E08 | long_term | FAIL | 366.5 | 0 | 100.0% | ApiError: headers: {'date': 'Mon, 17 Aug 2026 16:57:25 GMT', 'content-type': 'text/plain; charset=utf-8', 'content-length': '13', 'connection': 'keep-alive', 'vary': 'Origin', 'x-content-type-options': 'nosniff', 'strict-transport-security': 'max-age=2592000', 'cf-cache-status': 'DYNAMIC', 'server': 'cloudflare', 'cf-ray': 'a2ca37bdfb51e2ff-HKG'}, status_code: 401, body: unauthorized
 |

## Evidence excerpts

### E01 - short_term

`<RECENT_TURNS> user: Ten du an ca nhan cua toi la ORCHID-27. Toi thich Python va khong thich Java. Khi giai thich code, hay dung vi du ngan. assistant: Da hieu: demo ca nhan ORCHID-27, uu tien Python, tranh Java, vi du ngan. user: Toi dang hoc async/await va hay nham coroutine voi Task. Neu sau nay gap chu de nay, hay giai thich bang timeline. assistant: Toi se uu tien timeline khi giai thich coroutine va Task. user: TODO: hoan thanh benchmark report truoc thu Sau luc 16:00. Day la open loop LAB-REPORT-1600. </RECENT_TURNS>`

### E06 - semantic

``

### E09 - long_term

``

### E10 - short_term

`<SESSION_SUMMARY> user: Constraint: REVIEW-DEADLINE-1600 - project review is Friday at 16:00 and must not be forgotten. | assistant: Acknowledged review constraint. | user: Filler turn 1 about UI spacing. | assistant: Filler answer 1. | user: Filler turn 2 about naming. | assistant: Filler answer 2. | user: Filler turn 3 about logging. | assistant: Filler answer 3. </SESSION_SUMMARY> <DURABLE_NOTES> - user: Constraint: REVIEW-DEADLINE-1600 - project review is Friday at 16:00 and must not be forgotten. - assistant: Acknowledged review constraint. </DURABLE_NOTES> <RECENT_TURNS> user: Filler turn 4 about tests. assistant: Filler answer 4. user: Filler turn 5 about docs. assistant: Filler answe`

### E02 - long_term

``

### E03 - long_term

``

### E04 - episodic

``

### E05 - episodic

``

### E07 - mixed

``

### E11 - semantic

``

### E08 - long_term

``
