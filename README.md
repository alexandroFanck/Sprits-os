# **Sprits-OS / LFN – Versão 0.3**

Sprits-OS (LFN – Linux From Nothing) é uma distribuição Linux minimalista construída totalmente do zero, com o objetivo de oferecer um ambiente simples, leve, transparente e totalmente personalizável para desenvolvedores, entusiastas e criadores de sistemas operacionais.

A versão **0.3** traz melhorias importantes no toolchain base, possibilitando compilar mais softwares e expandir a distro de forma segura e modular.

---

## 🧩 **Componentes adicionados na versão 0.3**

A versão **0.3** inclui o conjunto essencial de ferramentas GNU para permitir a construção, modificação e expansão do sistema:

* **Glibc**
* **GCC & libstdc++**
* **Make**
* **Tar**
* **Gzip**
* **Sed**
* **Grep**
* **Awk**
* **Binutils**
* **XZ Utils**

Esses pacotes formam o núcleo de um ambiente de desenvolvimento básico que permite compilar aplicações, manipular arquivos e personalizar o sistema.

---

### ✔ Para modificar a distro:

1. Monte o disk.img.
2. O kernel atual (`bzImage`) foi configurado para usar **o mínimo de recursos**, por isso:

   * Se quiser incluir drivers, sistemas de arquivos extras ou funcionalidades adicionais, será necessário **recompilar o kernel**.

---

## 💽 **Usando o `disk.img`**

O arquivo **disk.img** pode ser utilizado de duas maneiras:

### ▶ 1. Em uma máquina virtual

Compatível com:

* QEMU
* VirtualBox (convertendo a imagem)
* VMware (convertendo a imagem)

Para iniciar no QEMU:

```bash
qemu-system-i386 -hda disk.img -m 1G
```

### 💾 2. Em hardware real

Você pode gravar diretamente em um pendrive/disco:

⚠ *Cuidado: isso apagará o dispositivo escolhido.*

```bash
sudo dd if=disk.img of=/dev/sdX bs=4M status=progress
sync
```

---

## 🛠️ **Objetivo do projeto**

A LFN / Sprits-OS foi criada para:

* Servir como base para aprendizado de sistemas Linux
* Ser um sistema minimalista para experimentos
* Permitir a criação de distribuições personalizadas
* Funcionarem bem em máquinas antigas ou de poucos recursos
* Explorar compilações manuais do kernel e do userspace

---

## 📌 **Estado Atual**

* Sistema **bootável via GRUB Legacy**
* Kernel mínimo funcional
* Toolchain GNU instalado
* `disk.img` pronto para virtualização ou gravação

---

## 📅 **Próximas versões (planejado)**

* Criar um init mais robusto
* Adicionar suporte a módulos externos do kernel
* Criar um instalador simples

---

## 🤝 **Contribuições**

Contribuições são bem-vindas!
Relate problemas, sugira melhorias ou envie pull requests.
