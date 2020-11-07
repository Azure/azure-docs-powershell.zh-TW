---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: 8a0fbc09f9c46bea6ac09d75911ac83b68f0e296
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966179"
---
# <span data-ttu-id="1898a-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="1898a-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="1898a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1898a-102">SYNOPSIS</span></span>
<span data-ttu-id="1898a-103">這個命令會列出所指定備份專案的連續記錄鏈起點和終點。</span><span class="sxs-lookup"><span data-stu-id="1898a-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="1898a-104">使用它來判斷使用者想要還原資料庫的時間點是否有效或不正確。</span><span class="sxs-lookup"><span data-stu-id="1898a-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="1898a-105">句法</span><span class="sxs-lookup"><span data-stu-id="1898a-105">SYNTAX</span></span>

### <span data-ttu-id="1898a-106">NoFilterParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1898a-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1898a-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="1898a-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1898a-108">說明</span><span class="sxs-lookup"><span data-stu-id="1898a-108">DESCRIPTION</span></span>
<span data-ttu-id="1898a-109">**AzRecoveryServicesBackupRecoveryLogChain** Cmdlet 會取得備份的 Azure 備份專案在時間範圍內的復原點。</span><span class="sxs-lookup"><span data-stu-id="1898a-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="1898a-110">在專案已備份之後， **AzRecoveryServicesBackupRecoveryLogChain** 物件有一個或多個還原時間範圍。</span><span class="sxs-lookup"><span data-stu-id="1898a-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="1898a-111">示例</span><span class="sxs-lookup"><span data-stu-id="1898a-111">EXAMPLES</span></span>

### <span data-ttu-id="1898a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="1898a-112">Example 1</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="1898a-113">第一個命令會從七天前取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="1898a-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="1898a-114">第二個命令會取得今天的日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="1898a-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="1898a-115">第三個命令會取得 AzureWorkload 備份容器，並將它們儲存在 $Containers 變數中。</span><span class="sxs-lookup"><span data-stu-id="1898a-115">The third command gets AzureWorkload backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="1898a-116">第四個命令會取得備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="1898a-116">The fourth command gets the backup item, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="1898a-117">最後一個命令會針對 $BackupItem 中的專案取得復原點時間範圍陣列，然後將它們儲存在 $RP 變數中。</span><span class="sxs-lookup"><span data-stu-id="1898a-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="1898a-118">參數</span><span class="sxs-lookup"><span data-stu-id="1898a-118">PARAMETERS</span></span>

### <span data-ttu-id="1898a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1898a-119">-DefaultProfile</span></span>
<span data-ttu-id="1898a-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1898a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1898a-121">-結束日期</span><span class="sxs-lookup"><span data-stu-id="1898a-121">-EndDate</span></span>
<span data-ttu-id="1898a-122">需要回遷復原點之時間範圍的結束時間</span><span class="sxs-lookup"><span data-stu-id="1898a-122">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="1898a-123">-專案</span><span class="sxs-lookup"><span data-stu-id="1898a-123">-Item</span></span>
<span data-ttu-id="1898a-124">需要取得復原點的受保護的專案物件</span><span class="sxs-lookup"><span data-stu-id="1898a-124">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="1898a-125">-開始日期</span><span class="sxs-lookup"><span data-stu-id="1898a-125">-StartDate</span></span>
<span data-ttu-id="1898a-126">需要回遷復原點之時間範圍的開始時間</span><span class="sxs-lookup"><span data-stu-id="1898a-126">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="1898a-127">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1898a-127">-VaultId</span></span>
<span data-ttu-id="1898a-128">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="1898a-128">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1898a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1898a-129">CommonParameters</span></span>
<span data-ttu-id="1898a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1898a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1898a-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1898a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1898a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1898a-132">INPUTS</span></span>

### <span data-ttu-id="1898a-133">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="1898a-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="1898a-134">System.object</span><span class="sxs-lookup"><span data-stu-id="1898a-134">System.String</span></span>

## <span data-ttu-id="1898a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1898a-135">OUTPUTS</span></span>

### <span data-ttu-id="1898a-136">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="1898a-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="1898a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1898a-137">NOTES</span></span>

## <span data-ttu-id="1898a-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1898a-138">RELATED LINKS</span></span>
