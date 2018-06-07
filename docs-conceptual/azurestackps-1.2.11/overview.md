---
title: Azure Stack PowerShell 概觀 | Microsoft Docs
description: Azure Stack PowerShell 安裝和設定概觀。
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: 3f55ff613004f0726e20255126b29bf7f64662b8
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820188"
---
# <a name="azure-stack-powershell"></a>Azure Stack PowerShell

Azure Stack 需要下列兩個 PowerShell 模組：  

1. Azure Stack 相容的 **AzureRM** 模組，可藉由安裝 **2017-03-09-profile** API 版本設定檔來取得。 使用此設定檔安裝的 Cmdlet 只可供 Azure Stack 操作員和使用者使用。

2. 最近的版本為 **1.2.11** 安裝 **AzureStack** 模組。 使用此模組安裝的 Cmdlet 只可供 Azure Stack 操作員使用。 操作員可以使用此模組所提供的 PowerShell Cmdlet 來執行各項作業，例如管理供應項目、方案、服務、配額等。 若要了解此模組中可用的 PowerShell Cmdlet，請參閱 [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) 和 [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) 參考內容。

## <a name="next-steps"></a>後續步驟

* [安裝 Azure Stack 適用的 PowerShell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [設定 PowerShell 以便搭配 Azure Stack 使用](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
