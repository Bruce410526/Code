记录从化学名转成SMILES常用的三种方法

  - 在化合物库搜索栏中直接检索：
    常用化合物数据库：
      a. PubChem(https://pubchem.ncbi.nlm.nih.gov/)
      b. ChEMBL(https://www.ebi.ac.uk/chembl/)
    优点：简单方便，不需要安装额外的工具
    缺点：并不是所有的化合物都能检索到，批量搜索比较麻烦
    
  - 使用软件转换
    例如ChemDraw,复制化合物名称，打开软件右击，选择Convert Name to Structure 显示出分子图，右击选择Molecule下的Copy As 找到SMILES即可得到对应的SMILES
    优点：化合物不局限于数据库，范围大大扩展
    缺点：需要额外安装软件，一次只能转换一个
    
  - 利用python库opsin
    需要先安装opsin：pip install opsin
    下载opsin-cli-2.7.0-jar-with-dependencies.jar ：url(https://github.com/dan2097/opsin/releases)
    示例命令：java -jar opsin-cli-2.7.0-jar-with-dependencies.jar -osmi input.txt output.txt
      其中input.txt中保存化学名称，一行对应一个化合物；output.txt是保存转换后SMILES的文件
