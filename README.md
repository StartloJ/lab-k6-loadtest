# lab-k6-loadtest

PoC demo learning how to use K6. We can learn more [here](https://k6.io/docs/get-started)

## Fast lane to get started

Execute mode has 2 sections.

1. API testing mode: read more [here](https://k6.io/docs/using-k6/http-requests/)
2. Browser testing mode: read more [here](https://k6.io/docs/using-k6-browser/overview/)

Example steps.

1. Install k6 simple binary [here](https://k6.io/docs/get-started/installation/)
2. Run example script
   
    ```bash
    k6 run examples/test-k6.js
    ```

3. Run example browser load

    ```bash
    k6 run examples/browser-k6.js
    # or
    K6_BROWSER_HEADLESS=false k6 run examples/browser-k6.js
    ```

## Feature focus

We can extend feature on K6(core service) with customize extension that you can explore more [here](https://k6.io/docs/extensions/)

1. **Output metrics**:  
   We can seamless integrate output result to 3th party. Read more [here](https://k6.io/docs/get-started/results-output/).  
   For experimental output, We found limitations that you need to build customize package for include function like a plugins or extensions. Read more [here](https://github.com/grafana/xk6-output-prometheus-remote)
2. **Browser base testing**:
    Read more to understanding how can we measurement [here](https://web.dev/vitals/#core-web-vitals)

## Advanced integrate

1. K6 integrate output result on Grafana dashboard. You can run docker compose to execute script and send result metrics to virtualize on Grafana below. Then, you can open browser and see your test result on `http://localhost:3000`

    ```bash
    cd scenarios/grafana-integrate
    docker compose up
    ```