---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 676ba76cb4412e03c684be4d166e8707c5652b26
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276595"
---
# <span data-ttu-id="c10a9-101">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="c10a9-101">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="c10a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c10a9-102">SYNOPSIS</span></span>

<span data-ttu-id="c10a9-103">取得已備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="c10a9-103">Gets the recovery points for a backed up item.</span></span>

## <span data-ttu-id="c10a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="c10a9-104">SYNTAX</span></span>

### <span data-ttu-id="c10a9-105">NoFilterParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c10a9-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c10a9-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="c10a9-106">DateTimeFilter</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>] [-Item] <ItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c10a9-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="c10a9-107">RecoveryPointId</span></span>
```
Get-AzRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c10a9-108">說明</span><span class="sxs-lookup"><span data-stu-id="c10a9-108">DESCRIPTION</span></span>

<span data-ttu-id="c10a9-109">**AzRecoveryServicesBackupRecoveryPoint** Cmdlet 會取得已備份之 Azure 備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="c10a9-109">The **Get-AzRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="c10a9-110">在已備份專案之後， **AzureRmRecoveryServicesBackupRecoveryPoint** 物件有一個或多個復原點。</span><span class="sxs-lookup"><span data-stu-id="c10a9-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>
<span data-ttu-id="c10a9-111">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="c10a9-111">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="c10a9-112">示例</span><span class="sxs-lookup"><span data-stu-id="c10a9-112">EXAMPLES</span></span>

### <span data-ttu-id="c10a9-113">範例1：從最後一周取得某個專案的復原點</span><span class="sxs-lookup"><span data-stu-id="c10a9-113">Example 1: Get recovery points from the last week for an item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime() -VaultId $vault.ID
```

<span data-ttu-id="c10a9-114">第一個命令會根據 vaultName 取得 vault 物件。</span><span class="sxs-lookup"><span data-stu-id="c10a9-114">The first command gets vault object based on vaultName.</span></span> <span data-ttu-id="c10a9-115">第二個命令會從七天前取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="c10a9-115">The second command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>
<span data-ttu-id="c10a9-116">第三個命令會取得今天的日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="c10a9-116">The third command gets today's date, and then stores it in the $EndDate variable.</span></span>
<span data-ttu-id="c10a9-117">第四個命令會取得！，然後將它們儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="c10a9-117">The fourth command gets AzureVM backup containers, and stores them in the $Container variable.</span></span> <span data-ttu-id="c10a9-118">第五個命令會根據 workloadType （vaultId）來取得備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="c10a9-118">The fifth command gets the backup item based on workloadType, vaultId and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="c10a9-119">最後一個命令會在 $BackupItem 中取得該專案的復原點數陣列，然後將它們儲存在 $RP 變數中。</span><span class="sxs-lookup"><span data-stu-id="c10a9-119">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="c10a9-120">參數</span><span class="sxs-lookup"><span data-stu-id="c10a9-120">PARAMETERS</span></span>

### <span data-ttu-id="c10a9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c10a9-121">-DefaultProfile</span></span>

<span data-ttu-id="c10a9-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c10a9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c10a9-123">-結束日期</span><span class="sxs-lookup"><span data-stu-id="c10a9-123">-EndDate</span></span>

<span data-ttu-id="c10a9-124">指定日期範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="c10a9-124">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="c10a9-125">-專案</span><span class="sxs-lookup"><span data-stu-id="c10a9-125">-Item</span></span>

<span data-ttu-id="c10a9-126">指定此 Cmdlet 取得復原點的專案。</span><span class="sxs-lookup"><span data-stu-id="c10a9-126">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="c10a9-127">若要取得 **AzureRmRecoveryServicesBackupItem** 物件，請使用 **AzRecoveryServicesBackupItem** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c10a9-127">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the **Get-AzRecoveryServicesBackupItem** cmdlet.</span></span>

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

### <span data-ttu-id="c10a9-128">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="c10a9-128">-KeyFileDownloadLocation</span></span>

<span data-ttu-id="c10a9-129">指定要下載輸入檔案以還原加密虛擬機器之 KeyVault 金鑰的位置。</span><span class="sxs-lookup"><span data-stu-id="c10a9-129">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="c10a9-130">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="c10a9-130">-RecoveryPointId</span></span>

<span data-ttu-id="c10a9-131">指定復原點 ID。</span><span class="sxs-lookup"><span data-stu-id="c10a9-131">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="c10a9-132">-開始日期</span><span class="sxs-lookup"><span data-stu-id="c10a9-132">-StartDate</span></span>

<span data-ttu-id="c10a9-133">指定日期範圍的開始日期。</span><span class="sxs-lookup"><span data-stu-id="c10a9-133">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="c10a9-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c10a9-134">-VaultId</span></span>

<span data-ttu-id="c10a9-135">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="c10a9-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c10a9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c10a9-136">CommonParameters</span></span>
<span data-ttu-id="c10a9-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c10a9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c10a9-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c10a9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c10a9-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c10a9-139">INPUTS</span></span>

### <span data-ttu-id="c10a9-140">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="c10a9-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="c10a9-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c10a9-141">System.String</span></span>

## <span data-ttu-id="c10a9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c10a9-142">OUTPUTS</span></span>

### <span data-ttu-id="c10a9-143">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="c10a9-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="c10a9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c10a9-144">NOTES</span></span>

## <span data-ttu-id="c10a9-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c10a9-145">RELATED LINKS</span></span>

[<span data-ttu-id="c10a9-146">AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="c10a9-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="c10a9-147">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="c10a9-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)
