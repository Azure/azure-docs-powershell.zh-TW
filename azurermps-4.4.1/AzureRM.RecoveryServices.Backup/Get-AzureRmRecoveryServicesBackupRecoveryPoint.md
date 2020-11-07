---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 838026E4-F001-434C-86F0-B2A838E93A9C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupRecoveryPoint.md
ms.openlocfilehash: 43ad564f261c423882b144d3fd9fbceba1273bcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625976"
---
# <span data-ttu-id="1bf73-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="1bf73-101">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>

## <span data-ttu-id="1bf73-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1bf73-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf73-103">取得已備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="1bf73-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bf73-104">句法</span><span class="sxs-lookup"><span data-stu-id="1bf73-104">SYNTAX</span></span>

### <span data-ttu-id="1bf73-105">NoFilterParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1bf73-105">NoFilterParameterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1bf73-106">DateTimeFilter</span><span class="sxs-lookup"><span data-stu-id="1bf73-106">DateTimeFilter</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bf73-107">RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="1bf73-107">RecoveryPointId</span></span>
```
Get-AzureRmRecoveryServicesBackupRecoveryPoint [-Item] <ItemBase> [-RecoveryPointId] <String>
 [[-KeyFileDownloadLocation] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bf73-108">說明</span><span class="sxs-lookup"><span data-stu-id="1bf73-108">DESCRIPTION</span></span>
<span data-ttu-id="1bf73-109">**AzureRmRecoveryServicesBackupRecoveryPoint** Cmdlet 會取得已備份之 Azure 備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="1bf73-109">The **Get-AzureRmRecoveryServicesBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="1bf73-110">在已備份專案之後， **AzureRmRecoveryServicesBackupRecoveryPoint** 物件有一個或多個復原點。</span><span class="sxs-lookup"><span data-stu-id="1bf73-110">After an item has been backed up, an **AzureRmRecoveryServicesBackupRecoveryPoint** object has one or more recovery points.</span></span>

<span data-ttu-id="1bf73-111">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1bf73-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1bf73-112">示例</span><span class="sxs-lookup"><span data-stu-id="1bf73-112">EXAMPLES</span></span>

### <span data-ttu-id="1bf73-113">範例1：從最後一周取得某個專案的復原點</span><span class="sxs-lookup"><span data-stu-id="1bf73-113">Example 1: Get recovery points from the last week for an item</span></span>
```
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM 
PS C:\> $RP = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

<span data-ttu-id="1bf73-114">第一個命令會從七天前取得日期，然後將它儲存在 $StartDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="1bf73-114">The first command gets the date from seven days ago, and then stores it in the $StartDate variable.</span></span>

<span data-ttu-id="1bf73-115">第二個命令會取得今天的日期，然後將它儲存在 $EndDate 變數中。</span><span class="sxs-lookup"><span data-stu-id="1bf73-115">The second command gets today's date, and then stores it in the $EndDate variable.</span></span>

<span data-ttu-id="1bf73-116">第三個命令會取得！，然後將它們儲存在 $Containers 變數中。</span><span class="sxs-lookup"><span data-stu-id="1bf73-116">The third command gets AzureVM backup containers, and stores them in the $Containers variable.</span></span>

<span data-ttu-id="1bf73-117">第四個命令會取得名為 V2VM 的備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="1bf73-117">The fourth command gets the backup item named V2VM, and then stores it in the $BackupItem variable.</span></span>

<span data-ttu-id="1bf73-118">最後一個命令會在 $BackupItem 中取得該專案的復原點數陣列，然後將它們儲存在 $RP 變數中。</span><span class="sxs-lookup"><span data-stu-id="1bf73-118">The last command gets an array of recovery points for the item in $BackupItem, and then stores them in the $RP variable.</span></span>

## <span data-ttu-id="1bf73-119">參數</span><span class="sxs-lookup"><span data-stu-id="1bf73-119">PARAMETERS</span></span>

### <span data-ttu-id="1bf73-120">-結束日期</span><span class="sxs-lookup"><span data-stu-id="1bf73-120">-EndDate</span></span>
<span data-ttu-id="1bf73-121">指定日期範圍的結尾。</span><span class="sxs-lookup"><span data-stu-id="1bf73-121">Specifies the end of the date range.</span></span>

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

### <span data-ttu-id="1bf73-122">-專案</span><span class="sxs-lookup"><span data-stu-id="1bf73-122">-Item</span></span>
<span data-ttu-id="1bf73-123">指定此 Cmdlet 取得復原點的專案。</span><span class="sxs-lookup"><span data-stu-id="1bf73-123">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="1bf73-124">若要取得 **AzureRmRecoveryServicesBackupItem** 物件，請使用 Get-AzureRmRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1bf73-124">To obtain an **AzureRmRecoveryServicesBackupItem** object, use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="1bf73-125">-KeyFileDownloadLocation</span><span class="sxs-lookup"><span data-stu-id="1bf73-125">-KeyFileDownloadLocation</span></span>
<span data-ttu-id="1bf73-126">指定要下載輸入檔案以還原加密虛擬機器之 KeyVault 金鑰的位置。</span><span class="sxs-lookup"><span data-stu-id="1bf73-126">Specifies the location to download the input file to restore the KeyVault key for an encrypted virtual machine.</span></span>

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

### <span data-ttu-id="1bf73-127">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="1bf73-127">-RecoveryPointId</span></span>
<span data-ttu-id="1bf73-128">指定復原點 ID。</span><span class="sxs-lookup"><span data-stu-id="1bf73-128">Specifies the recovery point ID.</span></span>

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

### <span data-ttu-id="1bf73-129">-開始日期</span><span class="sxs-lookup"><span data-stu-id="1bf73-129">-StartDate</span></span>
<span data-ttu-id="1bf73-130">指定日期範圍的開始日期。</span><span class="sxs-lookup"><span data-stu-id="1bf73-130">Specifies the start of the date range.</span></span>

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

### <span data-ttu-id="1bf73-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf73-131">-DefaultProfile</span></span>
<span data-ttu-id="1bf73-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bf73-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bf73-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf73-133">CommonParameters</span></span>
<span data-ttu-id="1bf73-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1bf73-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf73-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1bf73-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf73-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1bf73-136">INPUTS</span></span>

### <span data-ttu-id="1bf73-137">ItemBase</span><span class="sxs-lookup"><span data-stu-id="1bf73-137">ItemBase</span></span>
<span data-ttu-id="1bf73-138">形參 "Item" 接受管線中 "ItemBase" 類型的值</span><span class="sxs-lookup"><span data-stu-id="1bf73-138">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="1bf73-139">輸出</span><span class="sxs-lookup"><span data-stu-id="1bf73-139">OUTPUTS</span></span>

### <span data-ttu-id="1bf73-140">RecoveryPointBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="1bf73-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="1bf73-141">[System.object]. RecoveryServices [RecoveryPointBase] 的 [] （.]）</span><span class="sxs-lookup"><span data-stu-id="1bf73-141">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase]</span></span>

## <span data-ttu-id="1bf73-142">筆記</span><span class="sxs-lookup"><span data-stu-id="1bf73-142">NOTES</span></span>

## <span data-ttu-id="1bf73-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bf73-143">RELATED LINKS</span></span>

[<span data-ttu-id="1bf73-144">AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="1bf73-144">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="1bf73-145">AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="1bf73-145">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


