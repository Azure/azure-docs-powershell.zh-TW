---
title: Azure Stack Admin PowerShell 概觀 | Microsoft Docs
description: Azure Stack Admin PowerShell 的概觀以及有關安裝和設定的指示。
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 03/04/2020
ms.openlocfilehash: 0ee905b741c9f79b4f831bb4ea628f97566b2f1d
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427270"
---
# <a name="azure-stack-module-181"></a><span data-ttu-id="719f6-103">Azure Stack 模組 1.8.1</span><span class="sxs-lookup"><span data-stu-id="719f6-103">Azure Stack Module 1.8.1</span></span>

## <a name="requirements"></a><span data-ttu-id="719f6-104">需求：</span><span class="sxs-lookup"><span data-stu-id="719f6-104">Requirements:</span></span>

<span data-ttu-id="719f6-105">最低支援的 Azure Stack 版本為 1910 版。</span><span class="sxs-lookup"><span data-stu-id="719f6-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="719f6-106">注意:如需較舊版的 Azure Stack 請查看[安裝 Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="719f6-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="719f6-107">安裝</span><span class="sxs-lookup"><span data-stu-id="719f6-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.1
```

## <a name="release-notes"></a><span data-ttu-id="719f6-108">版本資訊</span><span class="sxs-lookup"><span data-stu-id="719f6-108">Release Notes</span></span>

* <span data-ttu-id="719f6-109">由 1910 更新所支援</span><span class="sxs-lookup"><span data-stu-id="719f6-109">Supported with 1910 update</span></span>