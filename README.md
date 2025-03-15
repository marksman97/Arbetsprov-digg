# Arbetsprov-digg

<h2 id="förutsättningar">Förutsättningar</h2>
<p>För att kunna köra filerna med kubectl och kustomize behöver du installera kubectl: https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/</p>
<p>Kubectl har stöd för kustomize så ingen extra installation krävs för det.</p>

<h2 id="köra-provet">För att köra med kustomize i kubectl</h2>
<p>För att köra med base mappen enbart när ni står i huvud mappen så är det detta kommandot: kubectl kustomize grunduppgifterna/base/</p>
<p>För att köra med prod enbart så är det kommandot: kubectl kustomize grunduppgifterna/overlays/prod/</p>

<h2 id="log-level">Log level</h2>
<p>I filen application.properties: quarkus.log.level=${LOG_LEVEL:info}<p>
<p>1. Quarkus applikationen kommer först och främst respektera miljövariabeln LOG_LEVEL.</p>
<p>2. Om miljövariabeln LOG_LEVEL inte finns (vilket det inte gör i till exempel bygg pipeline) så kommer applikationen att falla tillbaka till att logga på info nivå. </p>
<p>oc set env deployment/arbetsprov-app LOG_LEVEL="info"</p>