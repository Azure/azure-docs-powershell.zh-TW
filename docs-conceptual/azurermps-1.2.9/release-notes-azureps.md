---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: c57ba563b5a4d4d19944fe8eca2cb4244ee5ed9e
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819706"
---
# <a name="release-notes"></a>版本資訊

這是此版本中對 Azure PowerShell 所做的變更清單。

## <a name="version-129"></a>1.2.9 版

此版本變更

* AzureRm.AzureStackAdmin 模組
    + 變更 Add-AzureRmResourceProviderRegistration Cmdlet 以支援系統管理員 Azure Resource Manager 和租用戶 Azure Resource Manager 分割 已新增 -ResourceManagerType 參數。
    + 移除每個 Cmdlet 中的 -AdminUri、-ApiVersion, -SubscriptionId 和 -Token 參數。 我們一直列印這些參數將會被淘汰且現在已移除的警告。
* AzureStackStorage 模組
    + 已新增 Cmdlet 來支援容器移轉案例。
    + 已移除參考內部元件和基礎功能的 Cmdlet。
* AzureRM.BootStrapper
    + 建立新的模組，以利用版本設定檔來管理 Azure PowerShell Cmdlet 的版本