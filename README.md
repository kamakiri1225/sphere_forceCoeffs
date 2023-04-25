# sphere_forceCoeffsff

## ブログ記事

以下は中級レベルですがPythonを使った自動化を行いたい方はご参考ください。

- [【OpenFOAM球体周りの抗力係数(1)】FreeCADで球体モデルを作る](https://takun-physics.net/13410/)
- [【OpenFOAM球体周りの抗力係数(2)】blockMesh内で変数定義でベースメッシュ作成](https://takun-physics.net/13421/)
- [【OpenFOAM球体周りの抗力係数(3)】snappyHexMeshで球体周りのメッシュ作成](https://takun-physics.net/13438/)
- [【OpenFOAM球体周りの抗力係数(4)】simpleFoamで定常解析でシミュレーション](https://takun-physics.net/13458/)
- [【OpenFOAM球体周りの抗力係数(5)】Pythonでパラメータスタディ](https://takun-physics.net/13482/)
![image](https://user-images.githubusercontent.com/36812492/226588547-534d6dd2-c17a-4085-bf1c-cb1a4566e082.png)


## blockMeshで球体周りの抗力係数(007_case)
```bash
cd 001_mesh
cd 001_inner
blockMesh
cd ../002_outer
blockMesh
cd ..
cp -r 001_inner 003_merge
mergeMeshes -overwrite 003_merge 002_outer
cd ../002_cyclicAMI_run
changeDictionary
extrudeMesh
simpleFoam > log.simpleFoam &
```

1. [【回転するバスケットボールまわりの流れ(1)】FreeCADで作るバスケットボール](https://takun-physics.net/13185/)
2. [【回転するバスケットボールまわりの流れ(2)】ボール周辺をblockMeshでメッシュ作成](https://takun-physics.net/14594/)
3. [【回転するバスケットボールまわりの流れ(3)】外部領域をblockMeshでメッシュ作成](https://takun-physics.net/15983/)
4. [【回転するバスケットボールまわりの流れ(4)】OpenFOAMで無回転の球体まわりの流れ](https://takun-physics.net/16006/)
5. [【回転するバスケットボールまわりの流れ(5)】球体周りの抗力係数が文献値と合わない原因](https://takun-physics.net/16043/)
