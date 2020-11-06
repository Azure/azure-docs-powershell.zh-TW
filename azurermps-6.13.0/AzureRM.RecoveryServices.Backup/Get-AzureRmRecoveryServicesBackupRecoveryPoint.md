---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: d9c53d550f64b17a7ee821b43322dd974b7b5676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450180"
---
# <span data-ttu-id="e8c02-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e8c02-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="e8c02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8c02-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c02-103">取得已備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="e8c02-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8c02-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8c02-104">SYNTAX</span></span>

### <span data-ttu-id="e8c02-105">NoFilterParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e8c02-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8c02-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="e8c02-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8c02-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="e8c02-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8c02-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8c02-108">DESCRIPTION</span></span>
<span data-ttu-id="e8c02-109">**AzureRmRecoveryServicesBackupRecoveryPoint** Cmdlet 會取得已備份之 Azure 備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="e8c02-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="e8c02-110">在已備份專案之後， **AzureRmRecoveryServicesBackupRecoveryPoint** 物件有一個或多個復原點。</span><span class="sxs-lookup"><span data-stu-id="e8c02-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="e8c02-111">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8c02-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="e8c02-112">示例</span><span class="sxs-lookup"><span data-stu-id="e8c02-112">EXAMPLES</span></span>

### <span data-ttu-id="e8c02-113">範例1：從最後一周取得某個專案的復原點</span><span class="sxs-lookup"><span data-stu-id="e8c02-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="e8c02-114">第一個命令會從七天前取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="e8c02-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="e8c02-115">第二個命令會取得今天的日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="e8c02-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="e8c02-116">第三個命令會取得！，然後將它們儲存在 $Containers 變數中。</span><span class="sxs-lookup"><span data-stu-id="e8c02-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>
<span data-ttu-id="e8c02-117">第四個命令會取得名為 V2VM 的備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="e8c02-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e8c02-118">最後一個命令會在 $BackupItem 中取得該專案的復原點數陣列，然後將它們儲存在 $RP 變數中。</span><span class="sxs-lookup"><span data-stu-id="e8c02-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="e8c02-119">參數</span><span class="sxs-lookup"><span data-stu-id="e8c02-119">PARAMETERS</span></span>

### <span data-ttu-id="e8c02-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c02-120">-DefaultProfile</span></span>
<span data-ttu-id="e8c02-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8c02-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8c02-122">-結束日期</span><span class="sxs-lookup"><span data-stu-id="e8c02-122">-EndDate</span></span>
<span data-ttu-id="e8c02-123">指定日期範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="e8c02-123">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="e8c02-124">-專案</span><span class="sxs-lookup"><span data-stu-id="e8c02-124">-Item</span></span>
<span data-ttu-id="e8c02-125">指定此 Cmdlet 取得復原點的專案。</span><span class="sxs-lookup"><span data-stu-id="e8c02-125">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="e8c02-126">若要取得 **AzureRmRecoveryServicesBackupItem** 物件，請使用 Get-AzureRmRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8c02-126">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="e8c02-127">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="e8c02-127">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="e8c02-128">指定要下載輸入檔案以還原加密虛擬機器之 KeyVault 金鑰的位置。</span><span class="sxs-lookup"><span data-stu-id="e8c02-128">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="e8c02-129">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="e8c02-129">-RecoveryPointId</span></span>
<span data-ttu-id="e8c02-130">指定復原點 ID。</span><span class="sxs-lookup"><span data-stu-id="e8c02-130">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="e8c02-131">-開始日期</span><span class="sxs-lookup"><span data-stu-id="e8c02-131">-StartDate</span></span>
<span data-ttu-id="e8c02-132">指定日期範圍的開始日期。</span><span class="sxs-lookup"><span data-stu-id="e8c02-132">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="e8c02-133">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e8c02-133">-VaultId</span></span>
<span data-ttu-id="e8c02-134">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="e8c02-134">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e8c02-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c02-135">CommonParameters</span></span>
<span data-ttu-id="e8c02-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8c02-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c02-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8c02-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c02-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e8c02-138">INPUTS</span></span>

### <span data-ttu-id="e8c02-139">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="e8c02-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="e8c02-140">參數： (ByValue 的專案) </span><span class="sxs-lookup"><span data-stu-id="e8c02-140">Parameters: Item (ByValue)</span></span>

### <span data-ttu-id="e8c02-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e8c02-141">System.String</span></span>
<span data-ttu-id="e8c02-142">參數： VaultId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e8c02-142">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="e8c02-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e8c02-143">OUTPUTS</span></span>

### <span data-ttu-id="e8c02-144">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="e8c02-144">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="e8c02-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e8c02-145">NOTES</span></span>

## <span data-ttu-id="e8c02-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8c02-146">RELATED LINKS</span></span>

[<span data-ttu-id="e8c02-147">AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e8c02-147">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="e8c02-148">AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e8c02-148">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


