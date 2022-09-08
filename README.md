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

   - Utilizado GLTFLoader para a criação de modelo de um macaco em 3D fazendo um import para utilizá-lo: 
   
      import {GLTFLoader} from 'three/examples/jsm/loaders/GLTFLoader.js';
    
      Exemplo:
    
     const assetLoader = new GLTFLoader();
     
      assetLoader.load(monkeyUrl.href, function(gltf) {
      
      const model = gltf.scene;
      
      console.log(model.children[1].material.opacity)
      
      scene.add(model);
      
      model.position.set(-12, 4, 10);

      mixer = new THREE.AnimationMixer( model );
      
      const clips = gltf.animations;

      const clip = THREE.AnimationClip.findByName( clips, 'myAnimation' );
      
      const action = mixer.clipAction( clip );

      }

- Realize a criação de objetos dinâmicos
  
   - AddBox
  
   - AddPlane
  
   - AddSphere
  
    Linhas do código 92- 127

- Possua algum tipo de interação com o usuário (mouse ou teclado)

    Exemplos: 

   - GUI
      
      Mudar a cor da esfera com o mouse:
      
      gui.addColor(options, 'sphereColor').onChange(function(e){
     sphere.material.color.set(e);
      
      Selecionar a opção com o mouse para mudar a estrutura da esfera em "grades":
      
      gui.add(options, 'wireframe').onChange(function(e){
      sphere.material.wireframe = e;
      });


   - OrbitControls: Movimentação da câmera
    
    # Print
    
   ![image](https://user-images.githubusercontent.com/37126620/189206747-a6f0d6c8-1dbb-4c74-9f23-7a23df68f79a.png)
