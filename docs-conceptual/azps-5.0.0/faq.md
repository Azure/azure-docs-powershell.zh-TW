---
title: 常見問題集 (FAQ)
description: 關於 Azure PowerShell 的常見問題集。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407505"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="8ddb8-103">關於 Azure PowerShell 的常見問題集</span><span class="sxs-lookup"><span data-stu-id="8ddb8-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="8ddb8-104">什麼是 Azure PowerShell？</span><span class="sxs-lookup"><span data-stu-id="8ddb8-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="8ddb8-105">Azure PowerShell 是一組 Cmdlet，可讓您直接使用 PowerShell 管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="8ddb8-106">在 2018 年 12 月，Az PowerShell 模組已正式推出。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="8ddb8-107">這個模組現在是用來與 Azure 互動的建議 PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="8ddb8-108">若要深入了解 Az PowerShell 模組，請參閱[新的 Azure PowerShell Az 模組簡介](/powershell/azure/new-azureps-module-az)。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="8ddb8-109">如何停用 Azure PowerShell 中的中斷性變更警告訊息？</span><span class="sxs-lookup"><span data-stu-id="8ddb8-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="8ddb8-110">若要隱藏 Azure PowerShell 中的中斷性變更警告訊息，您必須將環境變數 `SuppressAzurePowerShellBreakingChangeWarnings` 設定為 `true`。</span><span class="sxs-lookup"><span data-stu-id="8ddb8-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
