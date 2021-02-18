---
title: Azure Az PowerShell 模組簡介
description: 介紹 Az PowerShell 模組，建議用於與 Azure 互動，並取代 AzureRM PowerShell 模組。
ms.date: 02/12/2021
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b52b6995fb50a6ce502d42e7df588ca72340a1e7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409472"
---
# <a name="introducing-the-azure-az-powershell-module"></a>Azure Az PowerShell 模組簡介

## <a name="overview"></a>概觀

Az PowerShell 模組是一組 Cmdlet，可直接從 PowerShell 管理 Azure 資源。 PowerShell 提供強大的自動化功能，可用於管理您的 Azure 資源，以取得 CI/CD 管線內容中的範例。

Az PowerShell 模組取代了 AzureRM，是用來與 Azure 互動的建議版本。

您可以使用 Az PowerShell 模組搭配下列其中一種方法：

* [透過 PowerShellGet 安裝 Az PowerShell 模組](install-az-ps.md) (建議選項)。
* [透過 MSI 安裝 Az PowerShell 模組](install-az-ps-msi.md)。
* [使用 Azure Cloud Shell](/azure/cloud-shell/overview)。
* [使用 Az PowerShell Docker 容器](azureps-in-docker.md)。

## <a name="features"></a>功能

Az PowerShell 模組具備下列優點：

* 安全性和穩定性
  * 權杖快取加密
  * 防止中間人攻擊類型
  * 支援使用 ADFS 2019 進行驗證
  * PowerShell 7 中的使用者名稱和密碼驗證
  * 支援連續存取評估等功能 (即將於 2021 推出)
* 支援所有 Azure 服務
  * 所有正式發行的 Azure 服務都有對應的支援 PowerShell 模組
  * 自 AzureRM 後的多個錯誤 (bug) 修正和 API 版本升級
* 新功能
  * Cloud Shell 和跨平台的支援
  * 可以取得及使用存取權杖來存取 Azure 資源
  * 適用於包含 Azure 資源進階 REST 作業的 Cmdlet

> [!NOTE]
> PowerShell 7 和更新版本是在所有平台上與 Az PowerShell 搭配使用的 PowerShell 建議版本。

Az PowerShell 是以 .NET Standard 程式庫為基礎，可以在所有平台 (包括 Windows、macOS 和 Linux) 上使用 PowerShell 7 和更新版本。 同時與 Windows PowerShell 5.1 相容。

我們致力於將 Azure 支援帶入所有平台，而所有 Az PowerShell 模組都可跨平台使用。

## <a name="upgrade-your-environment-to-az"></a>將您的環境升級至 Az

為了運用 PowerShell 中的最新 Azure 功能，您應盡速遷移至 Az 模組。 若您尚未準備好要安裝 Az 模組來取代 AzureRM，您可以透過下列方式試用 Az：

* 在 `PowerShell` 環境中使用 [Azure Cloud Shell](/azure/cloud-shell/overview)。 Azure Cloud Shell 是一種以瀏覽器為基礎的殼層環境，隨附有已安裝的 Az 模組，且已啟用 `Enable-AzureRM` 相容性別名。
* 保留 Windows PowerShell 5.1 中安裝的 AzureRM 模組，並在 PowerShell 7 或更新版本中安裝 Az 模組。 Windows PowerShell 5.1 和 PowerShell 7 以及更新版本分別使用不同的模組集合。 請依照指示安裝[最新版 PowerShell](/powershell/scripting/install/installing-powershell)，然後從 PowerShell 7 或更新版本[安裝 Az 模組](install-az-ps.md)。

若要從現有的 AzureRM 安裝升級：

1. [將 Azure PowerShell AzureRM 模組解除安裝](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)
1. [安裝 Azure PowerShell Az 模組](install-az-ps.md)
1. **選擇性**：當您熟悉新的命令集時，請使用 [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) 啟用相容性模式來新增 AzureRM Cmdlet 的別名。 如需詳細資訊，請參閱下一節或[開始從 AzureRM 移轉至 Az](migrate-from-azurerm-to-az.md)。

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a>將現有指令碼從 Azure RM 遷移至 Az

如果您的指令碼仍以 AzureRM 模組為基礎，我們有數個資源可協助您進行移轉：

* [開始從 AzureRM 移轉至 Az](migrate-from-azurerm-to-az.md)
* [從 AzureRM 到 Az 1.0.0 的重大變更完整清單](migrate-az-1.0.0.md)
* [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) Cmdlet

## <a name="supportability"></a>可支援性

Az 是最新的 Azure PowerShell 模組。 若有任何問題或功能要求，您可以直接記錄在 [GitHub 存放庫](https://github.com/Azure/azure-powershell)，如果擁有支援合約，則可透過 Microsoft 支援服務直接回報。 功能要求將會在最新版本的 Az 中實作。 重大問題將會在最新的兩個 Az 版本中實作。

由於 Az PowerShell 模組現在具備 AzureRM PowerShell 模組的所有功能，因此我們將于2024年2月29日淘汰 AzureRM PowerShell 模組。

若要避免服務中斷，請將使用 AzureRM PowerShell 模組的 [腳本更新為在](https://aka.ms/azpsmigrate) 2024 年2月29日之前使用 Az powershell 模組。 若要自動更新您的腳本，請遵循 [快速入門手冊](/powershell/azure/quickstart-migrate-azurerm-to-az-automatically)。

## <a name="data-collection"></a>資料集合

Azure PowerShell 預設會收集遙測資料。 Microsoft 彙總收集的資料，以識別使用模式、識別常見的問題，以及改善 Azure PowerShell 的體驗。
Microsoft Azure PowerShell 不會收集任何私人或個人資料。 例如，使用量資料有助於找出問題 (例如具有低成功率的 Cmdlet)，並協助設定工作的優先順序。

我們非常感謝這類資料所提供的見解，但也了解不是每個人都想要傳送使用資料。 您可以使用 [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection) Cmdlet 停用資料收集。 若要深入了解，您也可以閱讀我們的[隱私權聲明](https://privacy.microsoft.com/privacystatement)。
