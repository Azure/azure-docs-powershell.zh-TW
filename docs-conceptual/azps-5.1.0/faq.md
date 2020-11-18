---
title: 常見問題集 (FAQ)
description: 關於 Azure PowerShell 的常見問題集。
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715172"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>關於 Azure PowerShell 的常見問題集

## <a name="what-is-azure-powershell"></a>什麼是 Azure PowerShell？

Azure PowerShell 是一組 Cmdlet，可讓您直接使用 PowerShell 管理 Azure 資源。 在 2018 年 12 月，Az PowerShell 模組已正式推出。 這個模組現在是用來與 Azure 互動的建議 PowerShell 模組。 若要深入了解 Az PowerShell 模組，請參閱[新的 Azure PowerShell Az 模組簡介](/powershell/azure/new-azureps-module-az)。

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>如何停用 Azure PowerShell 中的中斷性變更警告訊息？

若要隱藏 Azure PowerShell 中的中斷性變更警告訊息，您必須將環境變數 `SuppressAzurePowerShellBreakingChangeWarnings` 設定為 `true`。

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
