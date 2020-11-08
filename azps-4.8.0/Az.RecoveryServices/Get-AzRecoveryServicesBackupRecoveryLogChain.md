---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136146"
---
# <span data-ttu-id="97ace-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span><span class="sxs-lookup"><span data-stu-id="97ace-101">Get-AzRecoveryServicesBackupRecoveryLogChain</span></span>

## <span data-ttu-id="97ace-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97ace-102">SYNOPSIS</span></span>
<span data-ttu-id="97ace-103">這個命令會列出所指定備份專案的連續記錄鏈起點和終點。</span><span class="sxs-lookup"><span data-stu-id="97ace-103">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="97ace-104">使用它來判斷使用者想要還原資料庫的時間點是否有效或不正確。</span><span class="sxs-lookup"><span data-stu-id="97ace-104">Use it to determine whether the point-in-time, to which the user wants the DB to be restored, is valid or not.</span></span>

## <span data-ttu-id="97ace-105">句法</span><span class="sxs-lookup"><span data-stu-id="97ace-105">SYNTAX</span></span>

### <span data-ttu-id="97ace-106">NoFilterParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="97ace-106">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97ace-107">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="97ace-107">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97ace-108">說明</span><span class="sxs-lookup"><span data-stu-id="97ace-108">DESCRIPTION</span></span>
<span data-ttu-id="97ace-109">**AzRecoveryServicesBackupRecoveryLogChain** Cmdlet 會取得備份的 Azure 備份專案在時間範圍內的復原點。</span><span class="sxs-lookup"><span data-stu-id="97ace-109">The **Get-AzRecoveryServicesBackupRecoveryLogChain** cmdlet gets the time range recovery points in time for a backed up Azure Backup item.</span></span>
<span data-ttu-id="97ace-110">在專案已備份之後， **AzRecoveryServicesBackupRecoveryLogChain** 物件有一個或多個還原時間範圍。</span><span class="sxs-lookup"><span data-stu-id="97ace-110">After an item has been backed up, an **AzRecoveryServicesBackupRecoveryLogChain** object has one or more recovery time ranges.</span></span>

## <span data-ttu-id="97ace-111">示例</span><span class="sxs-lookup"><span data-stu-id="97ace-111">EXAMPLES</span></span>

### <span data-ttu-id="97ace-112">範例1</span><span class="sxs-lookup"><span data-stu-id="97ace-112">Example 1</span></span>
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="97ace-113">第一個命令會從七天前取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="97ace-113">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="97ace-114">第二個命令會取得今天的日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="97ace-114">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="97ace-115">第三個命令會取得 AzureWorkload 備份容器，並將它們儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="97ace-115">The third command gets AzureWorkload backup containers, and stores them in the $Container variable.</span></span>
<span data-ttu-id="97ace-116">第四個命令會取得備份專案，然後透過輸送式 Cmdlet 將它共用為備份專案物件。</span><span class="sxs-lookup"><span data-stu-id="97ace-116">The fourth command gets the backup item, and then shares it across the piped cmdlet as backup item object.</span></span>
<span data-ttu-id="97ace-117">最後一個命令會針對 $BackupItem 中的專案取得復原點時間範圍陣列，然後將它們儲存在 $RP 變數中。</span><span class="sxs-lookup"><span data-stu-id="97ace-117">The last command gets an array of recovery point time ranges for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

### <span data-ttu-id="97ace-118">範例2</span><span class="sxs-lookup"><span data-stu-id="97ace-118">Example 2</span></span>

<span data-ttu-id="97ace-119">這個命令會列出所指定備份專案的連續記錄鏈起點和終點。</span><span class="sxs-lookup"><span data-stu-id="97ace-119">This command lists the start and end points of the unbroken log chain of the given backup item.</span></span> <span data-ttu-id="97ace-120"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="97ace-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="97ace-121">參數</span><span class="sxs-lookup"><span data-stu-id="97ace-121">PARAMETERS</span></span>

### <span data-ttu-id="97ace-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ace-122">-DefaultProfile</span></span>
<span data-ttu-id="97ace-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97ace-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97ace-124">-結束日期</span><span class="sxs-lookup"><span data-stu-id="97ace-124">-EndDate</span></span>
<span data-ttu-id="97ace-125">需要回遷復原點之時間範圍的結束時間</span><span class="sxs-lookup"><span data-stu-id="97ace-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="97ace-126">-專案</span><span class="sxs-lookup"><span data-stu-id="97ace-126">-Item</span></span>
<span data-ttu-id="97ace-127">需要取得復原點的受保護的專案物件</span><span class="sxs-lookup"><span data-stu-id="97ace-127">Protected Item object for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="97ace-128">-開始日期</span><span class="sxs-lookup"><span data-stu-id="97ace-128">-StartDate</span></span>
<span data-ttu-id="97ace-129">需要回遷復原點之時間範圍的開始時間</span><span class="sxs-lookup"><span data-stu-id="97ace-129">Start time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="97ace-130">-VaultId</span><span class="sxs-lookup"><span data-stu-id="97ace-130">-VaultId</span></span>
<span data-ttu-id="97ace-131">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="97ace-131">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="97ace-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ace-132">CommonParameters</span></span>
<span data-ttu-id="97ace-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97ace-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ace-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="97ace-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ace-135">輸入</span><span class="sxs-lookup"><span data-stu-id="97ace-135">INPUTS</span></span>

### <span data-ttu-id="97ace-136">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="97ace-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="97ace-137">System.object</span><span class="sxs-lookup"><span data-stu-id="97ace-137">System.String</span></span>

## <span data-ttu-id="97ace-138">輸出</span><span class="sxs-lookup"><span data-stu-id="97ace-138">OUTPUTS</span></span>

### <span data-ttu-id="97ace-139">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="97ace-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="97ace-140">筆記</span><span class="sxs-lookup"><span data-stu-id="97ace-140">NOTES</span></span>

## <span data-ttu-id="97ace-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="97ace-141">RELATED LINKS</span></span>
