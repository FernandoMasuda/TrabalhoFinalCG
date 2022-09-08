# TrabalhoFinalCG

- Utilize pelo menos 3 tipos diferentes de geometrias
  
  - boxGeometry
  
  - planeGeometry
  
  - sphereGeometry

- Utilize pelo menos 2 tipos de materiais

     Exemplos de materiais utilizados:

   - const boxMaterial = new THREE.MeshBasicMaterial
    
   - const sphereMaterial = new THREE.MeshStandardMaterial

- Carregue pelo menos 1 textura
    - textureLoader()
    
       Texturas utilizando as imagens "nebula.jpg", "stars.jpg"
    
- Possua pelo menos 2 fontes de iluminação
  
  - AmbientLight
  
  - SpotLight

- Carregue pelo menos um modelo externo

   - Utilizado GLTFLoader para a criação de modelo de um macaco em 3D
    
      Exemplo:
    
     const assetLoader = new GLTFLoader();

- Realize a criação de objetos dinâmicos
  
   - AddBox
  
   - AddPlane
  
   - AddSphere
  
    Linhas do código 92- 127

- Possua algum tipo de interação com o usuário (mouse ou teclado)

    Exemplos: 

   - GUI
    
      gui.addColor(options, 'sphereColor').onChange(function(e){
     sphere.material.color.set(e); - Mudar a cor da esfera com o mouse

      gui.add(options, 'wireframe').onChange(function(e){
      sphere.material.wireframe = e;
      }); - Selecionar a opção com o mouse para mudar a estrutura da esfera em "grades"


   - OrbitControls: Movimentação da câmera
    
    # Exemplo
    
    ![image](https://user-images.githubusercontent.com/37126620/189177685-95867909-332c-4000-b175-6e5750e94aa0.png)
