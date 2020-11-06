---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9838db99fa1126f3948bb16f9ee16180cb652904
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448275"
---
# <span data-ttu-id="2526e-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2526e-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="2526e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2526e-102">SYNOPSIS</span></span>
<span data-ttu-id="2526e-103">啟動備份專案的備份。</span><span class="sxs-lookup"><span data-stu-id="2526e-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2526e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2526e-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2526e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2526e-105">DESCRIPTION</span></span>
<span data-ttu-id="2526e-106">**AzureRmRecoveryServicesBackupItem** Cmdlet 會針對受保護的 Azure 備份專案（未與備份排程關聯）啟動備份。</span><span class="sxs-lookup"><span data-stu-id="2526e-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="2526e-107">您可以在啟用保護後立即執行初始備份，或在排程備份失敗後啟動備份。</span><span class="sxs-lookup"><span data-stu-id="2526e-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="2526e-108">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2526e-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2526e-109">示例</span><span class="sxs-lookup"><span data-stu-id="2526e-109">EXAMPLES</span></span>

### <span data-ttu-id="2526e-110">範例1：啟動備份專案的備份</span><span class="sxs-lookup"><span data-stu-id="2526e-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="2526e-111">第一個命令會取得類型為 pstestv2vm1 的備份容器，然後將它儲存在 $NamedContainer 變數中。</span><span class="sxs-lookup"><span data-stu-id="2526e-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="2526e-112">第二個命令會取得與 $NamedContainer 容器相對應的備份專案，然後將其儲存在 $Item 變數中。</span><span class="sxs-lookup"><span data-stu-id="2526e-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="2526e-113">最後一個命令會在 $Item 中觸發備份專案的備份作業。</span><span class="sxs-lookup"><span data-stu-id="2526e-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="2526e-114">參數</span><span class="sxs-lookup"><span data-stu-id="2526e-114">PARAMETERS</span></span>

### <span data-ttu-id="2526e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2526e-115">-DefaultProfile</span></span>
<span data-ttu-id="2526e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2526e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2526e-117">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="2526e-117">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="2526e-118">將到期時間指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="2526e-118">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2526e-119">-專案</span><span class="sxs-lookup"><span data-stu-id="2526e-119">-Item</span></span>
<span data-ttu-id="2526e-120">指定此 Cmdlet 啟動備份操作的備份專案。</span><span class="sxs-lookup"><span data-stu-id="2526e-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2526e-121">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2526e-121">-VaultId</span></span>
<span data-ttu-id="2526e-122">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="2526e-122">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2526e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="2526e-123">-Confirm</span></span>
<span data-ttu-id="2526e-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2526e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2526e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2526e-125">-WhatIf</span></span>
<span data-ttu-id="2526e-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2526e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2526e-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2526e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2526e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2526e-128">CommonParameters</span></span>
<span data-ttu-id="2526e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2526e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2526e-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2526e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2526e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2526e-131">INPUTS</span></span>

### <span data-ttu-id="2526e-132">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="2526e-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="2526e-133">參數： (ByValue 的專案) </span><span class="sxs-lookup"><span data-stu-id="2526e-133">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="2526e-134">系統. Nullable "1 [[System. DateTime，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2526e-134">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2526e-135">System.object</span><span class="sxs-lookup"><span data-stu-id="2526e-135">System.String</span></span>
<span data-ttu-id="2526e-136">參數： VaultId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="2526e-136">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="2526e-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2526e-137">OUTPUTS</span></span>

### <span data-ttu-id="2526e-138">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="2526e-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2526e-139">筆記</span><span class="sxs-lookup"><span data-stu-id="2526e-139">NOTES</span></span>

## <span data-ttu-id="2526e-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="2526e-140">RELATED LINKS</span></span>

[<span data-ttu-id="2526e-141">AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2526e-141">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="2526e-142">AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2526e-142">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="2526e-143">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2526e-143">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


