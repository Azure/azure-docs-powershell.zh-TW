---
title: Azure Stack Admin PowerShell 概觀 | Microsoft Docs
description: Azure Stack Admin PowerShell 的概觀以及有關安裝和設定的指示。
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "78264405"
---
# <a name="azure-stack-module-180"></a>Azure Stack 模組 1.8.0

## <a name="requirements"></a>需求：

最低支援的 Azure Stack 版本為 1910 版。

注意:如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)

## <a name="install"></a>安裝

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a>版本資訊

* 由 1910 更新所支援
* 這些變更包括：

    - **新的 DRP 管理模組**：部署資源提供者 (DRP) 可對 Azure Stack Hub 進行資源提供者的協調部署。 這些命令會與 Azure Resource Manager 層進行互動，進而與 DRP 進行互動。

    - **BRP**：
        - 支援 Azure stack 基礎結構備份的單一角色還原。
        - 將 `RoleName` 參數新增至 R`estore-AzsBackup` Cmdlet。

    - **FRP**：**磁碟機**和**磁碟區**的重大變更，並搭配 API 版本 2019-05-01。 Azure Stack Hub 1910 和更新版本所支援的功能：
        - 已變更 `Name`、`HealthStatus` 和 `OperationalStatus` 的值。
        - **磁碟機**資源支援新的屬性：`FirmwareVersion`、`IsIndicationEnabled`、`Manufacturer` 和 `StoragePool`。
        - **磁碟機**資源的屬性 `CanPool` 和 `CannotPoolReason` 已淘汰；請改用 `OperationalStatus`。
