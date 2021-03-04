---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: c0080985637e58232e2f7eea37344ab291d5d594
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908477"
---
# <span data-ttu-id="511a0-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="511a0-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="511a0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="511a0-102">SYNOPSIS</span></span>
<span data-ttu-id="511a0-103">此命令會列出所指備份專案之未斷記錄鏈的開始與結束點。</span><span class="sxs-lookup"><span data-stu-id="511a0-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="511a0-104">使用它來判斷使用者想要還原 DB 的時間點是否有效。</span><span class="sxs-lookup"><span data-stu-id="511a0-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="511a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="511a0-105">SYNTAX</span></span>

### <span data-ttu-id="511a0-106">NoFilterParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="511a0-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="511a0-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="511a0-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="511a0-108">描述</span><span class="sxs-lookup"><span data-stu-id="511a0-108">DESCRIPTION</span></span>
<span data-ttu-id="511a0-109">**Get-AzRecoveryServicesBackupRecoveryLogChain** Cmdlet 會取得備份的 Azure 備份專案的時程復原點。</span><span class="sxs-lookup"><span data-stu-id="511a0-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="511a0-110">備份專案之後 **，AzRecoveryServicesBackupRecoveryLogChain** 物件有一或多個復原時間範圍。</span><span class="sxs-lookup"><span data-stu-id="511a0-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="511a0-111">例子</span><span class="sxs-lookup"><span data-stu-id="511a0-111">EXAMPLES</span></span>

### <span data-ttu-id="511a0-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="511a0-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="511a0-113">第一個命令會從七天前開始獲得日期，然後將它儲存在$StartDate變數中。</span><span class="sxs-lookup"><span data-stu-id="511a0-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="511a0-114">第二個命令會獲得今天的日期，然後將它儲存在$EndDate變數。</span><span class="sxs-lookup"><span data-stu-id="511a0-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="511a0-115">第三個命令會獲得 AzureWorkload 備份容器，並儲存在$Container變數中。</span><span class="sxs-lookup"><span data-stu-id="511a0-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="511a0-116">第四個命令會獲得備份專案，然後在整個管道 Cmdlet 之間共用它做為備份專案物件。</span><span class="sxs-lookup"><span data-stu-id="511a0-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="511a0-117">最後一個命令會針對 $BackupItem 中的專案，獲得復原點時間範圍的陣列，然後將它們儲存在 $RP 變數中。</span><span class="sxs-lookup"><span data-stu-id="511a0-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="511a0-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="511a0-118">Example 2</span></span>

<span data-ttu-id="511a0-119">此命令會列出所指備份專案之未斷記錄鏈的開始與結束點。</span><span class="sxs-lookup"><span data-stu-id="511a0-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="511a0-120"> (自動) </span><span class="sxs-lookup"><span data-stu-id="511a0-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="511a0-121">參數</span><span class="sxs-lookup"><span data-stu-id="511a0-121">PARAMETERS</span></span>

### <span data-ttu-id="511a0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511a0-122">-DefaultProfile</span></span>
<span data-ttu-id="511a0-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="511a0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511a0-124">-EndDate</span><span class="sxs-lookup"><span data-stu-id="511a0-124">-EndDate</span></span>
<span data-ttu-id="511a0-125">需要抓取復原點之時間範圍的結束時間</span><span class="sxs-lookup"><span data-stu-id="511a0-125">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511a0-126">-專案</span><span class="sxs-lookup"><span data-stu-id="511a0-126">-Item</span></span>
<span data-ttu-id="511a0-127">需要抓取復原點之受保護的專案物件</span><span class="sxs-lookup"><span data-stu-id="511a0-127">Protected Item object for which recovery point need to be fetched</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="511a0-128">-StartDate</span><span class="sxs-lookup"><span data-stu-id="511a0-128">-StartDate</span></span>
<span data-ttu-id="511a0-129">需要抓取復原點的開始時間</span><span class="sxs-lookup"><span data-stu-id="511a0-129">Start time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="511a0-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="511a0-130">-VaultId</span></span>
<span data-ttu-id="511a0-131">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="511a0-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="511a0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511a0-132">CommonParameters</span></span>
<span data-ttu-id="511a0-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="511a0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511a0-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="511a0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511a0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="511a0-135">INPUTS</span></span>

### <span data-ttu-id="511a0-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="511a0-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="511a0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="511a0-137">System.String</span></span>

## <span data-ttu-id="511a0-138">輸出</span><span class="sxs-lookup"><span data-stu-id="511a0-138">OUTPUTS</span></span>

### <span data-ttu-id="511a0-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="511a0-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="511a0-140">筆記</span><span class="sxs-lookup"><span data-stu-id="511a0-140">NOTES</span></span>

## <span data-ttu-id="511a0-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="511a0-141">RELATED LINKS</span></span>
