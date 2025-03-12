# Arbetsprov-digg

<h2 id="förutsättningar">Förutsättningar</h2>
<p>För att kunna köra filerna med kubectl och kustomize behöver du installera kubectl: https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/</p>
<p>Kubectl har stöd för kustomize så ingen extra installation krävs för det.</p>

<h2 id="köra-provet">För att köra med kustomize i kubectl</h2>
<p>För att köra med base mappen enbart så är det kommandot: kubectl kustomize base/</p>
<p>För att köra med prod  enbart så är det kommandot: kubectl kustomize overlays/prod/</p>
