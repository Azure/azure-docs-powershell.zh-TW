---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 9e9aab3a71e976d9c41694702dae7a8087da9a36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906517"
---
# <span data-ttu-id="93fb0-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="93fb0-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="93fb0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="93fb0-102">SYNOPSIS</span></span>

<span data-ttu-id="93fb0-103">獲得備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="93fb0-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="93fb0-104">語法</span><span class="sxs-lookup"><span data-stu-id="93fb0-104">SYNTAX</span></span>

### <span data-ttu-id="93fb0-105">NoFilterParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="93fb0-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-UseSecondaryRegion] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93fb0-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="93fb0-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93fb0-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="93fb0-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93fb0-108">描述</span><span class="sxs-lookup"><span data-stu-id="93fb0-108">DESCRIPTION</span></span>

<span data-ttu-id="93fb0-109">**Get-AzRecoveryServicesBackupRecoveryPoint** Cmdlet 取得備份的 Azure 備份專案的修復點。</span><span class="sxs-lookup"><span data-stu-id="93fb0-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="93fb0-110">備份專案之後 **，AzureRmRecoveryServicesBackupRecoveryPoint** 物件會擁有一或多個修復點。</span><span class="sxs-lookup"><span data-stu-id="93fb0-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="93fb0-111">使用 -VaultId 參數設定庫上下文。</span><span class="sxs-lookup"><span data-stu-id="93fb0-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="93fb0-112">例子</span><span class="sxs-lookup"><span data-stu-id="93fb0-112">EXAMPLES</span></span>

### <span data-ttu-id="93fb0-113">範例 1：從上周取得專案的復原點數</span><span class="sxs-lookup"><span data-stu-id="93fb0-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="93fb0-114">第一個命令會以 vaultName 為基礎，獲得庫物件。</span><span class="sxs-lookup"><span data-stu-id="93fb0-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="93fb0-115">第二個命令會獲得七天前的日期，然後將它儲存在$StartDate變數。</span><span class="sxs-lookup"><span data-stu-id="93fb0-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="93fb0-116">第三個命令會獲得今天的日期，然後將它儲存在$EndDate變數。</span><span class="sxs-lookup"><span data-stu-id="93fb0-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="93fb0-117">第四個命令會獲得 AzureVM 備份容器，並儲存在$Container變數中。</span><span class="sxs-lookup"><span data-stu-id="93fb0-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="93fb0-118">第五個命令會依據工作負載類型、保存庫Id 來獲得備份專案，然後將它儲存在$BackupItem變數。</span><span class="sxs-lookup"><span data-stu-id="93fb0-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="93fb0-119">最後一個命令會針對 $BackupItem 中的專案獲得復原點陣列，然後將它們儲存在 $RP 變數中。</span><span class="sxs-lookup"><span data-stu-id="93fb0-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="93fb0-120">參數</span><span class="sxs-lookup"><span data-stu-id="93fb0-120">PARAMETERS</span></span>

### <span data-ttu-id="93fb0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93fb0-121">-DefaultProfile</span></span>

<span data-ttu-id="93fb0-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="93fb0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93fb0-123">-EndDate</span><span class="sxs-lookup"><span data-stu-id="93fb0-123">-EndDate</span></span>

<span data-ttu-id="93fb0-124">指定日期範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="93fb0-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="93fb0-125">-專案</span><span class="sxs-lookup"><span data-stu-id="93fb0-125">-Item</span></span>

<span data-ttu-id="93fb0-126">指定此 Cmdlet 會獲得修復點的專案。</span><span class="sxs-lookup"><span data-stu-id="93fb0-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="93fb0-127">若要取得 **AzureRmRecoveryServicesBackupItem** 物件，請使用 **Get-AzRecoveryServicesBackupItem** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93fb0-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="93fb0-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="93fb0-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="93fb0-129">指定下載輸入檔案的位置，以還原加密虛擬機器的 KeyVault 金鑰。</span><span class="sxs-lookup"><span data-stu-id="93fb0-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93fb0-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="93fb0-130">-RecoveryPointId</span></span>

<span data-ttu-id="93fb0-131">指定修復點識別碼。</span><span class="sxs-lookup"><span data-stu-id="93fb0-131">Specifies the recovery point ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RecoveryPointId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93fb0-132">-StartDate</span><span class="sxs-lookup"><span data-stu-id="93fb0-132">-StartDate</span></span>

<span data-ttu-id="93fb0-133">指定日期範圍的開始。</span><span class="sxs-lookup"><span data-stu-id="93fb0-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="93fb0-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="93fb0-134">-VaultId</span></span>

<span data-ttu-id="93fb0-135">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="93fb0-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="93fb0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93fb0-136">CommonParameters</span></span>
<span data-ttu-id="93fb0-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="93fb0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93fb0-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93fb0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93fb0-139">輸入</span><span class="sxs-lookup"><span data-stu-id="93fb0-139">INPUTS</span></span>

### <span data-ttu-id="93fb0-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="93fb0-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="93fb0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="93fb0-141">System.String</span></span>

## <span data-ttu-id="93fb0-142">輸出</span><span class="sxs-lookup"><span data-stu-id="93fb0-142">OUTPUTS</span></span>

### <span data-ttu-id="93fb0-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="93fb0-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="93fb0-144">筆記</span><span class="sxs-lookup"><span data-stu-id="93fb0-144">NOTES</span></span>

## <span data-ttu-id="93fb0-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="93fb0-145">RELATED LINKS</span></span>

[<span data-ttu-id="93fb0-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="93fb0-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="93fb0-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="93fb0-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
