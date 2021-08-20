# ansuz
to read yaml from git and apply it in gitops style


graph TB
subgraph Ansuz
  D1[kube:deploy]
  E1[env:'git:branch'] --> P1
  E3[env:'git:token'] --> P1
  E2[env:'folder'] --> P2
  I1[image:ansuz] --> D1
  D1 --> P1(git clone - perm!)
  P1 --> P2(scan folder - exist!)
  P2 --> P3(apply yaml - error!)
end
