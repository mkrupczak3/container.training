# Exercise — Helm charts

Let's write a Helm chart for wordsmith!

We will need the YAML manifests that we wrote earlier.

Level 1: create a chart to deploy wordsmith.

Level 2: make it so that the number of replicas can be set with `--set replicas=X`.

Level 3: change the colors of the lego bricks.

(For level 3, you'll have to build/push your own images.)

See next slide if you need hints!

---

## Hints

*Scroll one slide at a time to see hints.*

--

Use `helm create` to create a new chart.

--

Delete the content of the `templates` directory and put your YAML instead.

--

Install the resulting chart. Voilà!

--

Use `{{ .Values.replicas }}` in the YAML manifest for `words`.

--

Also add `replicas: 5` to `values.yaml` to provide a default value.

---

## Changing the color

- Create an account on e.g. Docker Hub (e.g. `janedoe`)

- Create an image repository (e.g. `janedoe/web`)

- Change the images and/or CSS in `web/static`

- Build and push

- Trigger a rolling update using the image you just pushed
