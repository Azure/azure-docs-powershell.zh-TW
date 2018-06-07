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
ms.openlocfilehash: 9f31fe404cca1162d5e4898287261f1bcbfa0f3a
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821848"
---
# <a name="release-notes"></a>版本資訊

這是此版本中對 Azure PowerShell 所做的變更清單。

## <a name="version-170"></a>1.7.0 版

* **所有 Cmdlet 的 -Force、–Confirm 和 $ConfirmPreference 參數行為變更我們正根據 PowerShell 指導方針變更此實作。對於大多數的 Cmdlet 而言，這表示移除 Force 參數，而要略過 ShouldProcess 提示，使用者必須在其 PowerShell 指令碼中包含 ‘-Confirm:$false’ 參數。** 此變更可處理下列問題︰
  - 正確實作 –WhatIf 功能，可讓使用者判斷 Cmdlet 或指令碼的效果，而不需進行任何實際的變更
  - 使用全工作階段的 $ConfirmPreference 控制提示，以便根據預期變更的影響來提示使用者 (如 Cmdlet 的 ConfirmImpact 設定所回報)
  - 使用 –Confirm 參數進行 Cmdlet 特有的確認提示控制
  - 在所有 Cmdlet 中一致使用 ShouldContinue 和 –Force 參數，僅適用於由於變更的特質而需要使用者提示的動作 (例如，刪除隱藏的檔案)
  - 與其他的 PowerShell Cmdlet 一致，其他 Cmdlet 的 PowerShell 指令碼知識會立即套用至 Azure PowerShell Cmdlet。

**請注意，現在要「自動略過所有情況下的所有提示」，Azure PowerShell Cmdlet 會要求使用者提供兩個參數︰**
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* Azure 計算
  - Set-AzureRmVMADDomainExtension
  - Get-AzureRmVMADDomainExtension
  - Restart-AzureVM 的 -Redeploy 參數
  - Move-AzureService、Move-AzureStorageAccount 和 Move-AzureVirtualNetwork 的 -Validate 參數
  - 如同以往，擴充 Cmdlet 的名稱和版本參數是選擇性的。
  - New-AzureVM 可以從 VM 物件取得授權類型。
* Azure 儲存體
  - 將 Tags 參數變更為 Tag，並新增參數別名 Tags
    + New-AzureRmStorageAccount
    + Set-AzureRmStorageAccount
* Azure 網路
  - 已針對虛擬網路對等互連新增 Cmdlet
* Azure Redis 快取
  - 已針對 Reset-AzureRmRedisCache 新增 Cmdlet
  - 已針對 Export-AzureRmRedisCache 新增 Cmdlet
  - 已針對 Import-AzureRmRedisCache 新增 Cmdlet
  - 已將 New-AzureRmRedisCache Cmdlet 修改為包含 vNet 的參數變更
* Azure SQL DB 備份/還原
  - LTR (長期保留) 備份功能的 Cmdlet
  - Get-AzureRmSqlServerBackupLongTermRetentionVault
  - Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Set-AzureRmSqlServerBackupLongTermRetentionVault
  - Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Restore-AzureRmSqlDatabase 現在支援已刪除資料庫的時間點還原
  - Restore-AzureRmSqlDatabase 現在支援從長期保留備份還原
* Azure LogicApp
  - 已新增 LogicApp 整合帳戶 Cmdlet。
  - Get-AzureRmIntegrationAccountAgreement
  - Get-AzureRmIntegrationAccountCallbackUrl
  - Get-AzureRmIntegrationAccountCertificate
  - Get-AzureRmIntegrationAccount
  - Get-AzureRmIntegrationAccountMap
  - Get-AzureRmIntegrationAccountPartner
  - Get-AzureRmIntegrationAccountSchema
  - New-AzureRmIntegrationAccountAgreement
  - New-AzureRmIntegrationAccountCertificate
  - New-AzureRmIntegrationAccount
  - New-AzureRmIntegrationAccountMap
  - New-AzureRmIntegrationAccountPartner
  - New-AzureRmIntegrationAccountSchema
  - Remove-AzureRmIntegrationAccountAgreement
  - Remove-AzureRmIntegrationAccountCertificate
  - Remove-AzureRmIntegrationAccount
  - Remove-AzureRmIntegrationAccountMap
  - Remove-AzureRmIntegrationAccountPartner
  - Remove-AzureRmIntegrationAccountSchema
  - Set-AzureRmIntegrationAccountAgreement
  - Set-AzureRmIntegrationAccountCertificate
  - Set-AzureRmIntegrationAccount
  - Set-AzureRmIntegrationAccountMap
  - Set-AzureRmIntegrationAccountPartner
  - Set-AzureRmIntegrationAccountSchema
* Azure Data Lake Store
  - 大幅改善檔案和資料夾上傳及下載的效能。
  - 這包括小幅變更參數名稱 (針對下載) 以及包含兩個新參數 (針對上傳)︰
    + NumThreads -> PerFileThreadCount，用來指出要在單一檔案中使用的執行緒數目
    + ConcurrentFileCount，用來指出要上傳/下載平行資料夾上傳/下載檔案數目。
  - 預設執行緒值現在的設計是針對大部分的檔案大小提供更理想的全面性輸送量。 如果效能不如預期，可以修改上述的值以符合需求。
* Azure Data Lake Analytics
  - 若未使用引數呼叫 Get-AzureRMDataLakeAnalyticsDataSource，現在會傳回所有的資料來源。
  - 這項變更也會從 Cmdlet 中移除資料來源類型參數。
  - 這項變更會導致使用下列屬性針對清單作業傳回新物件︰
    + Type：資料來源的類型
    + Name：資料來源的名稱
    + IsDefault：如果這是帳戶的預設資料來源，則設定為 true
  - Get-AzureRMDataLakeAnalyticsJob 已修正根據 submittedBefore 和 submittedAfter 篩選時，某些日期時間位移值的清單。
* Web Apps
  - 新增 Swap-AzureRmWebAppSlot Cmdlet 以便進行定期交換和使用預覽交換
  - 擴充 Set-AzureRmWebAppSlot Cmdlet 以支援自動交換
* Azure API 管理
  - 已修正 AzureChinaCloud 的 Azure Api 管理部署 Cmdlet。
  - 已移除 Cmdlet Set-AzureRmApiManagementTenantGitAccess，因為預設會啟用 Git 存取。
* Azure 復原服務備份
  - 已新增 Azure SQL 工作負載的支援
  - 已新增備份及還原已加密 Azure VM 的支援
  - Backup-AzureRmRecoveryServicesBackupItem - 已新增復原點的選擇性保留時間功能
  - Get-AzureRmRecoveryServicesBackupContainer 和 Get-AzureRmRecoveryServicesBackupItem Cmdlet 中的小幅篩選相關錯誤修正
* Azure 自動化
  - 已新增 Get-AzureRmAutomationHybridWorkerGroup
