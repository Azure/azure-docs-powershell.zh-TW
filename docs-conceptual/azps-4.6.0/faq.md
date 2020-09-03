---
title: 常見問題集 (FAQ)
description: 關於 Azure PowerShell 的常見問題集。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244478"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="151be-103">關於 Azure PowerShell 的常見問題集</span><span class="sxs-lookup"><span data-stu-id="151be-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="151be-104">什麼是 Azure PowerShell？</span><span class="sxs-lookup"><span data-stu-id="151be-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="151be-105">Azure PowerShell 是一組 Cmdlet，可讓您直接使用 PowerShell 管理 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="151be-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="151be-106">在 2018 年 12 月，Az PowerShell 模組已正式推出。</span><span class="sxs-lookup"><span data-stu-id="151be-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="151be-107">這個模組現在是用來與 Azure 互動的建議 PowerShell 模組。</span><span class="sxs-lookup"><span data-stu-id="151be-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="151be-108">若要深入了解 Az PowerShell 模組，請參閱[新的 Azure PowerShell Az 模組簡介](/powershell/azure/new-azureps-module-az)。</span><span class="sxs-lookup"><span data-stu-id="151be-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="151be-109">如何停用 Azure PowerShell 中的中斷性變更警告訊息？</span><span class="sxs-lookup"><span data-stu-id="151be-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="151be-110">若要隱藏 Azure PowerShell 中的中斷性變更警告訊息，您必須將環境變數 `SuppressAzurePowerShellBreakingChangeWarnings` 設定為 `true`。</span><span class="sxs-lookup"><span data-stu-id="151be-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
