# TFG-GANs

Repositorio para mi Trabajo Fin de Grado: **Fundamentos Matemáticos y Aplicaciones Prácticas de las Redes Generativas Antagónicas (GANs)**. Se trata de un TFG del Grado en Matemáticas por la Universidad de Alicante.

Tutor: Julen Rebollo Múgica

## Resumen

En este trabajo se ha realizado un estudio en profundidad de las Redes Generativas Antagónicas (GANs), una de las arquitecturas más innovadoras dentro del campo del aprendizaje profundo. Las GANs, introducidas por Ian Goodfellow en 2014, están formadas por dos redes neuronales enfrentadas en un juego minimax: un generador, encargado de producir datos sintéticos, y un discriminador, que trata de distinguir entre datos reales y generados. Se estudia cómo, a través de un proceso de entrenamiento conjunto y competitivo, se logra obtener tanto la mejor red generadora como la mejor red discriminadora posibles, alcanzando un equilibrio de Nash. Esta estructura ha demostrado una gran capacidad para aprender distribuciones complejas y generar datos altamente realistas, siendo especialmente relevante en ámbitos como la generación de imágenes, audio y vídeo. 

Para poder abordar el estudio de las GANs, se introduce inicialmente el concepto de red neuronal artificial, desde su unidad básica (la neurona) hasta arquitecturas más complejas. Se analizan las funciones de activación, fundamentales para dotar de no linealidad al modelo, y se detalla el algoritmo de *backpropagation*, pilar del proceso de aprendizaje mediante descenso del gradiente.

En el núcleo del trabajo, se expone el modelado teórico de las GANs, así como su proceso de entrenamiento y los principales retos que plantea este en la práctica. Entre las dificultades más relevantes se encuentran el desvanecimiento de gradientes y el colapso de modo. Para abordar estas limitaciones, se estudian distintas variantes y mejoras de la arquitectura original, como las Deep Convolutional GANs (DCGANs) y las StyleGANs, cada una con importantes contribuciones tanto teóricas como prácticas.

Además, se realiza una comparativa entre las GANs y otros modelos generativos del estado del arte, valorando su rendimiento y aplicabilidad en distintos contextos. Finalmente, se incluye el desarrollo práctico de una GAN, detallando su implementación, pruebas y resultados obtenidos.

Este trabajo pone de manifiesto la importancia de las GANs como modelos generativos por su notable velocidad en la generación de datos, lo que las convierte en una herramienta muy útil en aplicaciones que requieren eficiencia computacional. Aunque en la actualidad existen modelos que pueden superar a las GANs en calidad de salida, estas siguen siendo una referencia clave por su capacidad para aprender distribuciones complejas de forma rápida y efectiva.

**Palabras clave**: GANs (Redes Generativas Antagónicas), Redes Neuronales, Colapso de Modo, Desvanecimiento de Gradientes.

## Abstract

This work presents an in-depth study of Generative Adversarial Networks (GANs), one of the most innovative architectures in the field of deep learning. GANs, introduced by Ian Goodfellow in 2014, consist of two neural networks engaged in a minimax game: a generator, responsible for producing synthetic data, and a discriminator, which attempts to distinguish between real and generated data. We study how, through a joint and competitive training process, we can obtain both the best possible generating network and the best possible discriminating network, reaching a Nash equilibrium. This structure has shown a remarkable ability to learn complex distributions and generate highly realistic data, making it especially relevant in areas such as image, audio, and video generation.

To approach the study of GANs, the concept of an artificial neural network is introduced, starting from its basic unit (the neuron) to more complex architectures. Activation functions, essential for introducing non-linearity into the model, are analyzed, and the backpropagation algorithm, which underpins the learning process via gradient descent, is explained in detail.

At the core of the work, the theoretical modeling of GANs is presented, along with their training process and the main challenges that arise in practice. Among the most significant difficulties are vanishing gradients and mode collapse. To address these limitations, several variants and improvements of the original architecture are examined, such as Deep Convolutional GANs (DCGANs) and StyleGANs, each with important theoretical and practical contributions.

In addition, a comparison is made between GANs and other state-of-the-art generative models, evaluating their performance and applicability in different contexts. Finally, a practical implementation of a GAN is included, detailing its development, testing, and the results obtained.

This study highlights the importance of GANs as generative models due to their remarkable speed in data generation, making them a very useful tool in applications that demand computational efficiency. Although there are currently models that can surpass GANs in output quality, they remain a key reference due to their ability to learn complex distributions quickly and effectively.

**Key words**: GANs (Generative Adversarial Networks), Neural Networks, Mode Collapse, Vanishing Gradients.

## Índice

1. [**Introducción**](Introducción)

2. [**Redes Neuronales**](#redes-neuronales)
    1. [La unidad básica](#la-unidad-básica)
    2. [Redes neuronales](#redes-neuronales-1)
        1. [Funciones de activación](#funciones-de-activación)
    3. [Backpropagation](#backpropagation)

3. [**Redes Generativas Antagónicas**](#redes-generativas-antagónicas)
    1. [Modelaje](#modelaje)
    2. [Proceso de entrenamiento](#proceso-de-entrenamiento)
    3. [Limitaciones y problemas en la práctica](#limitaciones-y-problemas-en-la-práctica)
        1. [Desvanecimiento de Gradientes (*Vanishing gradients*)](#desvanecimiento-de-gradientes-vanishing-gradients)
        2. [Colapso de modo (*Mode Collapse*)](#colapso-de-modo-mode-collapse)
        3. [Soportes de Baja Dimensión](#soportes-de-baja-dimensión)
    4. [Evolución de las GANs](#evolución-de-las-gans)
        1. [DCGAN](#dcgan)
        2. [StyleGAN](#stylegan)
    5. [Aplicación y comparativa de las GANs frente a modelos actuales](#aplicación-y-comparativa-de-las-gans-frente-a-modelos-actuales)

4. [**Desarrollo práctico en python de una GAN**](#desarrollo-práctico-en-python-de-una-gan)
    1. [Estructura de la DCGAN](#estructura-de-la-dcgan)

5. [**Conclusión**](#conclusión)

6. [**Referencias**](#referencias)

A. [**Detalles del desarrollo del trabajo**](#detalles-del-desarrollo-del-trabajo)

B. [**Definiciones y Proposiciones adicionales**](#definiciones-y-proposiciones-adicionales)

C. [**Código Python utilizado**](#código-python-utilizado)


