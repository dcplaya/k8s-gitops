Sometimes Rook likes to make a bunch of PVs non-stop. I believe its because something is stuck in the helm operator.
This is the command I use to delete all released PVs (rook or not)
```
kubectl get pv | grep Released | awk '$1 {print$1}' | while read vol; do kubectl delete pv/${vol}; done
```
