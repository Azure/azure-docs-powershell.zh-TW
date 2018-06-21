---
title: 安裝和設定 Azure PowerShell 服務管理模組 | Microsoft Docs
description: 如何安裝並設定 Azure PowerShell 以供第一次使用。
services: azure
author: sdwheeler
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 164af369d49e3044e5409c28d8b6145ebc067313
ms.sourcegitcommit: 020066d68d4ab68da162a4ae0cb4e239241f950f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/28/2017
ms.locfileid: "20622551"
---
# <a name="installing-the-azure-powershell-service-management-module"></a>安裝 Azure PowerShell 服務管理模組

從 [PowerShell 資源庫](https://www.powershellgallery.com/)安裝 Azure PowerShell 是慣用的安裝方法。

## <a name="step-1-install-powershellget"></a>步驟 1：安裝 PowerShellGet

從 PowerShell 資源庫安裝項目需要有 PowerShellGet 模組。 確定您有適當版本的 PowerShellGet 及其他系統需求。 執行下列命令，以查看您的系統上是否已安裝 PowerShellGet。

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

您應該會看到類似下面的輸出：

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

如果您未安裝 PowerShellGet，請參閱[如何取得 PowerShellGet](#how-to-get-powershellget)。

## <a name="step-2-install-azure-powershell"></a>步驟 2：安裝 Azure PowerShell

從執行身分為系統管理員的 Windows PowerShell 主控台來執行下列命令︰

```powershell
Install-Module Azure
```

Azure 模組是 Azure Resource Manager Cmdlet 的彙總套件模組。 當您安裝 AzureRM 模組時，系統會從 PowerShell 資源庫下載並安裝先前未安裝的其他任何 Azure 模組。

Azure 服務管理模組會與 Azure PowerShell Resource Manager 模組共用相依性。 如果您已安裝 Azure PowerShell Resource Manager 模組，您必須在 install 命令中新增 `-AllowClobber` 參數。 這可讓這個現有的共用相依性進行更新。 如果沒有這個參數，模組的安裝會失敗。

```powershell
Install-Module Azure -AllowClobber
```

安裝此模組之後，您可以執行下列命令來匯入模組︰

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a>使用 Cmdlet

若要開始使用 Azure 服務管理 Cmdlet，請先登入您的 Azure 帳戶。 若要登入您的帳戶，請執行下列命令︰

```powershell
Add-AzureAccount
```

在登入 Azure 之後，Azure PowerShell 會建立給定工作階段的內容。 該內容會包含要用於該工作階段內所有 Cmdlet 的 Azure PowerShell 環境、帳戶、租用戶和訂用帳戶。 現在您已準備好使用下列模組。

## <a name="azure-service-management-cmdlets"></a>Azure 服務管理的 Cmdlet

Azure PowerShell 模組經常會更新。 如果您發現 Cmdlet 的線上說明包含模組中沒有的 Cmdlet 或參數，請下載並安裝最新版的模組。 若要尋找您的模組版本，請輸入︰`(Get-Module Azure).Version`。

如需相關指令碼範例來協助您在 Azure 中自動進行一些常見工作，請參閱 [Windows Azure 指令碼中心](http://www.windowsazure.com/documentation/scripts/)。

如需有關安裝、學習、使用和自訂 Windows PowerShell 的一般資訊，請參閱[使用 Windows PowerShell 來編寫指令碼](http://go.microsoft.com/fwlink/p/?linkid=320210)。

### <a name="how-to-get-powershellget"></a>如何取得 PowerShellGet

|作業系統版本|安裝指示|
|---|---|
|我有 Windows 10 或 Windows Server 2016|內建於 OS 包含的 Windows Management Framework (WMF) 5.0|
|我想要升級至 PowerShell 5|[安裝最新版的 WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|我是在採用 PowerShell 3 或 PowerShell 4 的 Windows 版本上執行|[取得 PackageManagement 模組](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>檢查 Azure PowerShell 的版本

雖然我們鼓勵您儘早升級至最新版本，但支援的 Azure PowerShell 版本有好幾個。 若要判斷已安裝的 Azure PowerShell 版本，請從命令列執行 `Get-Module AzureRM`。

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
