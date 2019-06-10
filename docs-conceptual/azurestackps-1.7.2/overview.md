---
title: Azure Stack Admin PowerShell 概觀 | Microsoft Docs
description: Azure Stack Admin PowerShell 的概觀以及有關安裝和設定的指示。
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855783"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="50f24-103">Azure Stack 模組 1.7.2</span><span class="sxs-lookup"><span data-stu-id="50f24-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="50f24-104">需求：</span><span class="sxs-lookup"><span data-stu-id="50f24-104">Requirements:</span></span>

<span data-ttu-id="50f24-105">最低支援的 Azure Stack 版本為 1904 版。</span><span class="sxs-lookup"><span data-stu-id="50f24-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="50f24-106">注意：如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="50f24-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install-powershell-for-azure-stack"></a><span data-ttu-id="50f24-107">安裝適用於 Azure Stack 的 PowerShell</span><span class="sxs-lookup"><span data-stu-id="50f24-107">Install PowerShell for Azure Stack</span></span>

<span data-ttu-id="50f24-108">安裝有三個步驟：</span><span class="sxs-lookup"><span data-stu-id="50f24-108">Installation has three steps:</span></span>

1. <span data-ttu-id="50f24-109">安裝 Azure Stack PowerShell 取決於 Azure Stack 的版本而定</span><span class="sxs-lookup"><span data-stu-id="50f24-109">Install Azure Stack PowerShell depending on your version of Azure Stack</span></span>
2. <span data-ttu-id="50f24-110">啟用其他儲存體功能</span><span class="sxs-lookup"><span data-stu-id="50f24-110">Enable additional storage features</span></span>
3. <span data-ttu-id="50f24-111">確認 PowerShell 的安裝</span><span class="sxs-lookup"><span data-stu-id="50f24-111">Confirm the installation of PowerShell</span></span>

### <a name="install-azure-stack-powershell"></a><span data-ttu-id="50f24-112">安裝 Azure Stack PowerShell</span><span class="sxs-lookup"><span data-stu-id="50f24-112">Install Azure Stack PowerShell</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a><span data-ttu-id="50f24-113">啟用其他儲存體功能</span><span class="sxs-lookup"><span data-stu-id="50f24-113">Enable additional storage features</span></span>

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a><span data-ttu-id="50f24-114">版本資訊</span><span class="sxs-lookup"><span data-stu-id="50f24-114">Release Notes</span></span>

* <span data-ttu-id="50f24-115">由 1904 更新所支援</span><span class="sxs-lookup"><span data-stu-id="50f24-115">Supported with 1904 update</span></span>
* <span data-ttu-id="50f24-116">這是重大變更版本。</span><span class="sxs-lookup"><span data-stu-id="50f24-116">This a breaking change release.</span></span> <span data-ttu-id="50f24-117">如需重大變更的詳細資訊，請參閱 <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="50f24-117">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="50f24-118">Azs.Backup.Admin 模組 \* 重大變更：備份對憑證型加密模式所做的變更。</span><span class="sxs-lookup"><span data-stu-id="50f24-118">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="50f24-119">對於對稱金鑰的支援已被取代。</span><span class="sxs-lookup"><span data-stu-id="50f24-119">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="50f24-120">Azs.Fabric.Admin Module       \* 描述           \* Get-AzsInfrastructureVolume 已淘汰，我們提供新的 Cmdlet Get-AzsVolume           \* Get-AzsStorageSystem 已淘汰，我們提供新的 Cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool 已淘汰，StorageSubSystem 物件具備容量屬性</span><span class="sxs-lookup"><span data-stu-id="50f24-120">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="50f24-121">Azs.Compute.Admin 模組           \* 錯誤修正：Add-AzsPlatformImage，Get-AzsPlatformImage：只在成功的路徑呼叫 ConvertTo-PlatformImageObject           \* 錯誤修正：Add-AzsVmExtension，Get-AzsVmExtension：只在成功的路徑呼叫 ConvertTo-VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="50f24-121">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="50f24-122">Azs.Storage.Admin 模組Module           \* 錯誤修正 - 若未提供，新的儲存體配額會使用預設值。」</span><span class="sxs-lookup"><span data-stu-id="50f24-122">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
