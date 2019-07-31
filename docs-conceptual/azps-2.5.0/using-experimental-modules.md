---
title: 使用實驗性 Azure PowerShell 模組
description: 了解實驗性 Azure PowerShell 模組的原理和使用方式。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: ae2fecf73271a34a08ac66de03962a7a529e353b
ms.sourcegitcommit: 6c0d296bfec7c1c35a1d15074ca5eacda6684ea4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2019
ms.locfileid: "68657581"
---
# <a name="use-experimental-azure-powershell-modules"></a>使用實驗性 Azure PowerShell 模組

Azure PowerShell 小組著重於 Azure 中的開發人員工具，正針對 Azure PowerShell 體驗的許多增強功能進行實驗。 本文說明如何選擇加入 Azure PowerShell 的實驗，並提供意見反應給開發小組。

## <a name="experimentation-methodology"></a>實驗方法

為簡化實驗，我們會建立新的 Azure PowerShell 模組，透過全新且更輕鬆的方式來實作現有的 Azure SDK 功能。 在大部分情況下，Cmdlet 會完全鏡像現有的 Cmdlet。 不過，實驗性 Cmdlet 會提供縮寫標記法和更有效率的預設值，讓您能更輕鬆地建立及管理 Azure 資源。

可透過現有的 Azure PowerShell 模組來並行安裝這些模組。 已將 Cmdlet 名稱縮短來提供較短的名稱，並防止名稱與現有的非實驗性 Cmdlet 發生衝突。

實驗性模組使用下列命名慣例：`Az.*.Experiments`. 此命名慣例類似於預覽模組的命名：`Az.*.Preview`。 預覽模組與實驗性模組不同。 預覽模組所實作的 Azure 服務新功能僅可作為預覽供應項目。 預覽模組會取代現有的 Azure PowerShell 模組，並使用相同的 Cmdlet 和參數名稱。

## <a name="how-to-install-an-experimental-module"></a>如何安裝實驗性模組

系統會將實驗性模組發佈至 PowerShell 資源庫，就如同現有的 Azure PowerShell 模組。 若要查看實驗模組清單，請執行下列命令：

```azurepowershell-interactive
Find-Module Az.*.Experiments
```

若要安裝實驗性模組，請使用 `Install-Module` Cmdlet。

### <a name="documentation-and-support"></a>文件與支援

文件會包含在安裝套件中，並可使用 `Get-Help` cmdlet 加以存取。 並未發行實驗性模組的官方文件。

建議您測試這些模組。 您的意見反應可讓我們改善可用性，並回應您的需求。 不過，由於目前為實驗階段，這些模組的支援很有限。 可在 GitHub 存放庫中建立[問題](https://github.com/Azure/azure-powershell/issues)來提交問題報告。

## <a name="experiments-and-areas-of-improvement"></a>增強功能的實驗和區域

這些增強功能是以競爭產品中的主要區別作為基礎來加以選取。 例如，Azure CLI 已提出關於_情節_而非 _API 介面區_的基礎命令論點。
Azure CLI 使用一系列的智慧型預設值，讓終端使用者能更輕鬆地進行「使用者入門」情節。

### <a name="core-improvements"></a>核心增強功能

核心增強功能會視為「常識」，且幾乎無須實驗即可繼續實作這些更新。

- 以情節作為基礎的 Cmdlet - *All  - cmdlet 都應針對情節而非 Azure REST 服務設計。

- 簡短名稱 - 包含 Cmdlet 的名稱以及參數的名稱。
  使用別名可與「舊的」Cmdlet 相容。 提供_回溯相容性_參數集。

- 智慧型預設值 - 建立智慧型預設值以填入「必要」資訊。 例如︰
  - 資源群組
  - Location
  - 相依資源

### <a name="experimental-improvements"></a>實驗性增強功能

實驗性增強功能所呈現的重大變更是小組需要透過實驗進行驗證的。

- 簡單類型 - 建立情節應遠離複雜類型和組態物件。 將組態簡化為一個或兩個參數。

- 「智慧型建立」- 所有實作「智慧型建立」的建立情節都必須_沒有_必要參數：Azure PowerShell 會以武斷的方式選擇所有必要的資訊。

- 灰色參數 - 在許多情況下，某些參數可能是「灰色」或半選擇性。 如果未指定參數，就會詢問使用者是否需要為他們產生參數。 灰色參數以使用者同意的內容作為基礎來推斷值，也是很合理的做法。
  例如，讓灰色參數建議最近使用過的值是很合理的做法。

- `-Auto` 參數 - `-Auto` 參數能為使用者提供「選擇加入」的方式來_預設所有事項_，同時維持主線路徑中必要參數的完整性。

### <a name="feature-specific-switches"></a>特定功能的參數

例如，「建立 web 應用程式」情節可能會有 `-Git` 或 `-AddRemote` 參數，能將 "azure" 遠端自動新增至現有的 Git 存放庫。

- 可設定的預設值 - 使用者應該能夠設定諸如 `-ResourceGroupName` 和 `-Location` 等特定通用參數的預設值。

- 大小的預設值 - 資源「大小」會混淆使用者，因為許多資源提供者都會使用不同的名稱 (例如，"Standard\_DS1\_v2" 或 "S1")。 不過，大部分使用者較關心的是成本。 以定價排程作為基礎來定義「通用」大小是合理的。 使用者可以選擇特定的大小，或是讓 Azure PowerShell 以資源預算作為基礎選擇_最佳選項_。

- 輸出格式 - Azure PowerShell 目前會傳回 `PSObject`，且幾乎沒有主控台輸出。 Azure PowerShell 需要向使用者顯示一些關於已使用的「智慧型預設值」資訊。
