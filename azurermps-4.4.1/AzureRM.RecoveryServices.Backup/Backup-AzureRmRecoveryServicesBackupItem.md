---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: acf448b58fdf7bcc218ece8b5fb2415bc30981ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625110"
---
# <span data-ttu-id="07c49-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="07c49-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="07c49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07c49-102">SYNOPSIS</span></span>
<span data-ttu-id="07c49-103">啟動備份專案的備份。</span><span class="sxs-lookup"><span data-stu-id="07c49-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07c49-104">句法</span><span class="sxs-lookup"><span data-stu-id="07c49-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07c49-105">說明</span><span class="sxs-lookup"><span data-stu-id="07c49-105">DESCRIPTION</span></span>
<span data-ttu-id="07c49-106">**AzureRmRecoveryServicesBackupItem** Cmdlet 會針對受保護的 Azure 備份專案（未與備份排程關聯）啟動備份。</span><span class="sxs-lookup"><span data-stu-id="07c49-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="07c49-107">您可以在啟用保護後立即執行初始備份，或在排程備份失敗後啟動備份。</span><span class="sxs-lookup"><span data-stu-id="07c49-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="07c49-108">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07c49-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="07c49-109">示例</span><span class="sxs-lookup"><span data-stu-id="07c49-109">EXAMPLES</span></span>

### <span data-ttu-id="07c49-110">範例1：啟動備份專案的備份</span><span class="sxs-lookup"><span data-stu-id="07c49-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="07c49-111">第一個命令會取得類型為 pstestv2vm1 的備份容器，然後將它儲存在 $NamedContainer 變數中。</span><span class="sxs-lookup"><span data-stu-id="07c49-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>

<span data-ttu-id="07c49-112">第二個命令會取得與 $NamedContainer 容器相對應的備份專案，然後將其儲存在 $Item 變數中。</span><span class="sxs-lookup"><span data-stu-id="07c49-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>

<span data-ttu-id="07c49-113">最後一個命令會在 $Item 中觸發備份專案的備份作業。</span><span class="sxs-lookup"><span data-stu-id="07c49-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="07c49-114">參數</span><span class="sxs-lookup"><span data-stu-id="07c49-114">PARAMETERS</span></span>

### <span data-ttu-id="07c49-115">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="07c49-115">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="07c49-116">將到期時間指定為 **DateTime** 物件。</span><span class="sxs-lookup"><span data-stu-id="07c49-116">Specifies an expiry time as a **DateTime** object.</span></span>

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

### <span data-ttu-id="07c49-117">-專案</span><span class="sxs-lookup"><span data-stu-id="07c49-117">-Item</span></span>
<span data-ttu-id="07c49-118">指定此 Cmdlet 啟動備份操作的備份專案。</span><span class="sxs-lookup"><span data-stu-id="07c49-118">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="07c49-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c49-119">-DefaultProfile</span></span>
<span data-ttu-id="07c49-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07c49-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07c49-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c49-121">CommonParameters</span></span>
<span data-ttu-id="07c49-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07c49-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c49-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07c49-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c49-124">輸入</span><span class="sxs-lookup"><span data-stu-id="07c49-124">INPUTS</span></span>

### <span data-ttu-id="07c49-125">DateTime</span><span class="sxs-lookup"><span data-stu-id="07c49-125">DateTime</span></span>
<span data-ttu-id="07c49-126">形參 "ExpiryDateTimeUTC" 接受管線中 "DateTime" 類型的值</span><span class="sxs-lookup"><span data-stu-id="07c49-126">Parameter 'ExpiryDateTimeUTC' accepts value of type 'DateTime' from the pipeline</span></span>

### <span data-ttu-id="07c49-127">ItemBase</span><span class="sxs-lookup"><span data-stu-id="07c49-127">ItemBase</span></span>
<span data-ttu-id="07c49-128">形參 "Item" 接受管線中 "ItemBase" 類型的值</span><span class="sxs-lookup"><span data-stu-id="07c49-128">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="07c49-129">輸出</span><span class="sxs-lookup"><span data-stu-id="07c49-129">OUTPUTS</span></span>

### <span data-ttu-id="07c49-130">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="07c49-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="07c49-131">筆記</span><span class="sxs-lookup"><span data-stu-id="07c49-131">NOTES</span></span>

## <span data-ttu-id="07c49-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="07c49-132">RELATED LINKS</span></span>

[<span data-ttu-id="07c49-133">AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="07c49-133">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="07c49-134">AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="07c49-134">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="07c49-135">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="07c49-135">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


