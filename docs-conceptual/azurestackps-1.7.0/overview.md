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
ms.openlocfilehash: 3daf7746dfc0e06c62209be0ffa164d657d91935
ms.sourcegitcommit: 4153218b2b51e42d6c3315bb7f0fcbcfac7d1f86
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/29/2019
ms.locfileid: "58616981"
---
# <a name="azure-stack-module-170"></a><span data-ttu-id="b9790-103">Azure Stack Module 1.7.0</span><span class="sxs-lookup"><span data-stu-id="b9790-103">Azure Stack Module 1.7.0</span></span>

## <a name="requirements"></a><span data-ttu-id="b9790-104">需求：</span><span class="sxs-lookup"><span data-stu-id="b9790-104">Requirements:</span></span>

<span data-ttu-id="b9790-105">最低支援的 Azure Stack 版本為 1901 版。</span><span class="sxs-lookup"><span data-stu-id="b9790-105">Minimum supported Azure Stack version is 1901.</span></span>

<span data-ttu-id="b9790-106">注意：如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="b9790-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="b9790-107">Install</span><span class="sxs-lookup"><span data-stu-id="b9790-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.0
```

## <a name="release-notes"></a><span data-ttu-id="b9790-108">版本資訊</span><span class="sxs-lookup"><span data-stu-id="b9790-108">Release Notes</span></span>

* <span data-ttu-id="b9790-109">由 1901 更新所支援</span><span class="sxs-lookup"><span data-stu-id="b9790-109">Supported with 1901 update</span></span>
* <span data-ttu-id="b9790-110">這是重大變更版本。</span><span class="sxs-lookup"><span data-stu-id="b9790-110">This a breaking change release.</span></span> <span data-ttu-id="b9790-111">如需重大變更的詳細資訊，請參閱 <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="b9790-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="b9790-112">Azs.Backup.Admin 模組 \* 重大變更：備份對憑證型加密模式所做的變更。</span><span class="sxs-lookup"><span data-stu-id="b9790-112">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="b9790-113">對於對稱金鑰的支援已被取代。</span><span class="sxs-lookup"><span data-stu-id="b9790-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="b9790-114">Azs.Fabric.Admin Module       \* 描述           \* Get-AzsInfrastructureVolume 已淘汰，我們提供新的 Cmdlet Get-AzsVolume           \* Get-AzsStorageSystem 已淘汰，我們提供新的 Cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool 已淘汰，StorageSubSystem 物件具備容量屬性</span><span class="sxs-lookup"><span data-stu-id="b9790-114">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="b9790-115">Azs.Compute.Admin 模組           \* 錯誤修正：Add-AzsPlatformImage，Get-AzsPlatformImage：只在成功的路徑呼叫 ConvertTo-PlatformImageObject           \* 錯誤修正：Add-AzsVmExtension，Get-AzsVmExtension：只在成功的路徑呼叫 ConvertTo-VmExtensionObject</span><span class="sxs-lookup"><span data-stu-id="b9790-115">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="b9790-116">Azs.Storage.Admin 模組Module           \* 錯誤修正 - 若未提供，新的儲存體配額會使用預設值。」</span><span class="sxs-lookup"><span data-stu-id="b9790-116">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
