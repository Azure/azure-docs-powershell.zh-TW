---
title: Azure Stack Admin PowerShell 概觀 | Microsoft Docs
description: Azure Stack Admin PowerShell 的概觀以及有關安裝和設定的指示。
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053310"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="d5ec8-103">Azure Stack 模組 1.6.0</span><span class="sxs-lookup"><span data-stu-id="d5ec8-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ec8-104">需求：</span><span class="sxs-lookup"><span data-stu-id="d5ec8-104">Requirements:</span></span>
<span data-ttu-id="d5ec8-105">支援的最低 Azure Stack 版本為 1811 版。</span><span class="sxs-lookup"><span data-stu-id="d5ec8-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="d5ec8-106">注意:如果您使用的是舊版，請安裝版本 1.6.0</span><span class="sxs-lookup"><span data-stu-id="d5ec8-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="d5ec8-107">安裝</span><span class="sxs-lookup"><span data-stu-id="d5ec8-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a><span data-ttu-id="d5ec8-108">版本資訊</span><span class="sxs-lookup"><span data-stu-id="d5ec8-108">Release Notes</span></span>
* <span data-ttu-id="d5ec8-109">由 1811 更新所支援</span><span class="sxs-lookup"><span data-stu-id="d5ec8-109">Supported with 1811 update</span></span>
* <span data-ttu-id="d5ec8-110">Azs.Compute.Admin 模組</span><span class="sxs-lookup"><span data-stu-id="d5ec8-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="d5ec8-111">修正 New-DataDiskObject 遺漏 Azs 前置詞的問題，並新增別名及未來將有取代項目的警告。</span><span class="sxs-lookup"><span data-stu-id="d5ec8-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="d5ec8-112">Azs.Update.Admin 模組</span><span class="sxs-lookup"><span data-stu-id="d5ec8-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="d5ec8-113">新增警告，建議您在執行 Install-AzsUpdate 之前先執行 Test-AzureStack</span><span class="sxs-lookup"><span data-stu-id="d5ec8-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="d5ec8-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="d5ec8-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="d5ec8-115">新 Cmdlet (Azure Stack 1811+ 支援的功能)</span><span class="sxs-lookup"><span data-stu-id="d5ec8-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="d5ec8-116">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="d5ec8-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="d5ec8-117">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="d5ec8-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="d5ec8-118">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="d5ec8-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="d5ec8-119">淘汰</span><span class="sxs-lookup"><span data-stu-id="d5ec8-119">Deprecation</span></span>
        * <span data-ttu-id="d5ec8-120">Get-AzsInfrastructureVolume 現在是 Get-AzsVolume Cmdlet 的別名</span><span class="sxs-lookup"><span data-stu-id="d5ec8-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="d5ec8-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="d5ec8-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="d5ec8-122">新增 Repair-AzsAlert Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d5ec8-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="d5ec8-123">Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="d5ec8-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="d5ec8-124">修正未使用預設配額值的錯誤</span><span class="sxs-lookup"><span data-stu-id="d5ec8-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="d5ec8-125">Azs.Subscriptions.Admin 模組</span><span class="sxs-lookup"><span data-stu-id="d5ec8-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="d5ec8-126">修正 New-AddonPlanDefinitionObject 遺漏 Azs 前置詞的問題，並新增別名及未來將有取代項目的警告。</span><span class="sxs-lookup"><span data-stu-id="d5ec8-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>
