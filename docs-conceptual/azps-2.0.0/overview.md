---
title: Azure PowerShell 的概觀
description: 概述 Azure PowerShell Az 模組，並有如何安裝和開始使用的相關資訊。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 45ab083dd133c8c7b8dbe902484c92564bc216b9
ms.sourcegitcommit: accff0c2cd6035fcda2d917f6051a5b509eb6255
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/06/2019
ms.locfileid: "65048745"
---
# <a name="overview-of-azure-powershell"></a>Azure PowerShell 的概觀

Azure PowerShell 提供了一組 Cmdlet，它們會使用 [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) 模型來管理 Azure 資源。 Azure PowerShell 會使用 .NET Standard，因此可供 Windows、macOS 和 Linux 使用。
Azure PowerShell 也可在 Azure Cloud Shell 取得。

## <a name="about-the-new-az-module"></a>關於新的 Az 模組

本文件說明適用於 Azure PowerShell 的新 Az 模組。 這個新模組是使用 .NET Standard 從頭開始撰寫的。 使用 .NET Standard 可讓 Azure PowerShell 在 Windows 上的 PowerShell 5 或任何平台上的 PowerShell 6 底下執行。 現在在透過 PowerShell 與 Azure 互動時，預期會採用 Az 模組。
AzureRM 仍可取得 Bug 修正，但不會再獲得新的功能。

請到 [Azure PowerShell Az 模組簡介](new-azureps-module-az.md)來了解新模組的完整詳細資料，包括命令重新命名的情形以及 AzureRM 的維護計劃。 如果您想要立即開始使用新的模組，請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md)。

您也可以取得 [AzureRM 文件](/powershell/azure/azurerm)。

> [!IMPORTANT]
>
> 雖然 Azure 文件將會進行更新以反映新的模組 Cmdlet 名稱，但相關文章可能仍會使用 AzureRM 命令。 在安裝 Az 模組之後，建議您使用 `Enable-AzureRmAlias` 啟用 AzureRM Cmdlet 別名。 請參閱[從 AzureRM 遷移至 Az](migrate-from-azurerm-to-az.md) 文章以取得詳細資料。

## <a name="run-or-install"></a>執行或安裝

您可以在 Windows 的 PowerShell 5.1 或更高版本，或任何平台的 PowerShell 6 上安裝 Azure PowerShell，或是在 Azure Cloud Shell 中加以執行。

* 若要在您的瀏覽器中使用 Azure Cloud Shell 執行，請參閱 [Azure Cloud Shell 中的 PowerShell 快速入門](/azure/cloud-shell/quickstart-powershell)。
* 若要在您的系統上安裝 Azure PowerShell，請參閱[安裝 Azure PowerShell](install-az-ps.md)。

如需最新 Azure PowerShell 版本的相關資訊，請參閱[版本資訊](release-notes-azureps.md)。

## <a name="get-started"></a>開始使用

請參閱[開始使用 Azure PowerShell](get-started-azureps.md) 文章，以了解 Azure PowerShell 基本概念。 如果您不熟悉 PowerShell，簡介可能會對您有所幫助：

* [安裝 PowerShell](/powershell/scripting/install/installing-powershell)
* [使用 PowerShell 編寫指令碼](/powershell/scripting/powershell-scripting)
* [PowerShell 基本概念：(第 1 部份) 開始使用 PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)
* Microsoft Virtual Academy 的[開始使用 PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)

下列範例說明 Azure 的一些常見用法：

* [Linux 虛擬機器](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Windows 虛擬機器](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a>透過 Microsoft Learn 增進您的技巧

- [使用 PowerShell 指令碼將 Azure 工作自動化](/learn/modules/automate-azure-tasks-with-powershell/)
- [更多互動式學習...](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>其他 Azure Powershell 模組

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
