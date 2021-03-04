---
title: 常見問題集 (FAQ)
description: 關於 Azure PowerShell 的常見問題集。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101881756"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="35021-103">關於 Azure PowerShell 的常見問題集</span><span class="sxs-lookup"><span data-stu-id="35021-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="35021-104">什麼是 Azure PowerShell？</span><span class="sxs-lookup"><span data-stu-id="35021-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="35021-105">Azure PowerShell 是一組 Cmdlet，可讓您直接使用 PowerShell 管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="35021-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="35021-106">在 2018 年 12 月，Az PowerShell 模組已正式推出。</span><span class="sxs-lookup"><span data-stu-id="35021-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="35021-107">這個模組現在是用來與 Azure 互動的建議 PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="35021-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="35021-108">若要深入了解 Az PowerShell 模組，請參閱[新的 Azure PowerShell Az 模組簡介](/powershell/azure/new-azureps-module-az)。</span><span class="sxs-lookup"><span data-stu-id="35021-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="35021-109">如何停用 Azure PowerShell 中的中斷性變更警告訊息？</span><span class="sxs-lookup"><span data-stu-id="35021-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="35021-110">若要隱藏 Azure PowerShell 中的中斷性變更警告訊息，您必須將環境變數 `SuppressAzurePowerShellBreakingChangeWarnings` 設定為 `true`。</span><span class="sxs-lookup"><span data-stu-id="35021-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
