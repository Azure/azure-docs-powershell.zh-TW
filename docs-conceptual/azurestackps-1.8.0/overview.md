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
# <a name="azure-stack-module-180"></a><span data-ttu-id="243c0-103">Azure Stack 模組 1.8.0</span><span class="sxs-lookup"><span data-stu-id="243c0-103">Azure Stack Module 1.8.0</span></span>

## <a name="requirements"></a><span data-ttu-id="243c0-104">需求：</span><span class="sxs-lookup"><span data-stu-id="243c0-104">Requirements:</span></span>

<span data-ttu-id="243c0-105">最低支援的 Azure Stack 版本為 1910 版。</span><span class="sxs-lookup"><span data-stu-id="243c0-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="243c0-106">注意:如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="243c0-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="243c0-107">安裝</span><span class="sxs-lookup"><span data-stu-id="243c0-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a><span data-ttu-id="243c0-108">版本資訊</span><span class="sxs-lookup"><span data-stu-id="243c0-108">Release Notes</span></span>

* <span data-ttu-id="243c0-109">由 1910 更新所支援</span><span class="sxs-lookup"><span data-stu-id="243c0-109">Supported with 1910 update</span></span>
* <span data-ttu-id="243c0-110">這些變更包括：</span><span class="sxs-lookup"><span data-stu-id="243c0-110">Changes include:</span></span>

    - <span data-ttu-id="243c0-111">**新的 DRP 管理模組**：部署資源提供者 (DRP) 可對 Azure Stack Hub 進行資源提供者的協調部署。</span><span class="sxs-lookup"><span data-stu-id="243c0-111">**New DRP Admin module**: The Deployment Resource Provider (DRP) enables orchestrated deployments of resource providers to Azure Stack Hub.</span></span> <span data-ttu-id="243c0-112">這些命令會與 Azure Resource Manager 層進行互動，進而與 DRP 進行互動。</span><span class="sxs-lookup"><span data-stu-id="243c0-112">These commands interact with the Azure Resource Manager layer to interact with DRP.</span></span>

    - <span data-ttu-id="243c0-113">**BRP**：</span><span class="sxs-lookup"><span data-stu-id="243c0-113">**BRP**:</span></span>
        - <span data-ttu-id="243c0-114">支援 Azure stack 基礎結構備份的單一角色還原。</span><span class="sxs-lookup"><span data-stu-id="243c0-114">Support single role restore for Azures stack infrastructure backup.</span></span>
        - <span data-ttu-id="243c0-115">將 `RoleName` 參數新增至 R`estore-AzsBackup` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="243c0-115">Add parameter `RoleName` to cmdlet R`estore-AzsBackup`.</span></span>

    - <span data-ttu-id="243c0-116">**FRP**：**磁碟機**和**磁碟區**的重大變更，並搭配 API 版本 2019-05-01。</span><span class="sxs-lookup"><span data-stu-id="243c0-116">**FRP**: Breaking changes for **Drive** and **Volume** resources with API version 2019-05-01.</span></span> <span data-ttu-id="243c0-117">Azure Stack Hub 1910 和更新版本所支援的功能：</span><span class="sxs-lookup"><span data-stu-id="243c0-117">The features are supported by Azure Stack Hub 1910 and later:</span></span>
        - <span data-ttu-id="243c0-118">已變更 `Name`、`HealthStatus` 和 `OperationalStatus` 的值。</span><span class="sxs-lookup"><span data-stu-id="243c0-118">The value of ID, `Name`, `HealthStatus`, and `OperationalStatus` have been changed.</span></span>
        - <span data-ttu-id="243c0-119">**磁碟機**資源支援新的屬性：`FirmwareVersion`、`IsIndicationEnabled`、`Manufacturer` 和 `StoragePool`。</span><span class="sxs-lookup"><span data-stu-id="243c0-119">Supported new properties `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`, and `StoragePool` for **Drive** resources.</span></span>
        - <span data-ttu-id="243c0-120">**磁碟機**資源的屬性 `CanPool` 和 `CannotPoolReason` 已淘汰；請改用 `OperationalStatus`。</span><span class="sxs-lookup"><span data-stu-id="243c0-120">The properties `CanPool` and `CannotPoolReason` of **Drive** resources have been deprecated; use `OperationalStatus` instead.</span></span>
