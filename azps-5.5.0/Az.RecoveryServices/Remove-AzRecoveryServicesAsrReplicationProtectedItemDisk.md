---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132319"
---
# <span data-ttu-id="3318a-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="3318a-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="3318a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3318a-102">SYNOPSIS</span></span>
<span data-ttu-id="3318a-103">移除受禁止複製專案的磁片。</span><span class="sxs-lookup"><span data-stu-id="3318a-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="3318a-104">句法</span><span class="sxs-lookup"><span data-stu-id="3318a-104">SYNTAX</span></span>

### <span data-ttu-id="3318a-105">AzureToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="3318a-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3318a-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="3318a-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3318a-107">說明</span><span class="sxs-lookup"><span data-stu-id="3318a-107">DESCRIPTION</span></span>
<span data-ttu-id="3318a-108">**AzRecoveryServicesAsrReplicationProtectedItemDisk** Cmdlet 會從 ASR 複製受保護的專案中移除磁片。</span><span class="sxs-lookup"><span data-stu-id="3318a-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="3318a-109">示例</span><span class="sxs-lookup"><span data-stu-id="3318a-109">EXAMPLES</span></span>

### <span data-ttu-id="3318a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3318a-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="3318a-111">啟動作業以從受管理的磁片的保護 VM 中移除指定磁片。</span><span class="sxs-lookup"><span data-stu-id="3318a-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="3318a-112">範例2</span><span class="sxs-lookup"><span data-stu-id="3318a-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="3318a-113">啟動作業，以從受管理的磁片移除保護 VM 中的指定磁片。</span><span class="sxs-lookup"><span data-stu-id="3318a-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="3318a-114">範例3</span><span class="sxs-lookup"><span data-stu-id="3318a-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="3318a-115">啟動作業以移除指定的磁片，並傳回用於追蹤 [移除受保護磁片] 作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="3318a-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="3318a-116">參數</span><span class="sxs-lookup"><span data-stu-id="3318a-116">PARAMETERS</span></span>

### <span data-ttu-id="3318a-117">-確認</span><span class="sxs-lookup"><span data-stu-id="3318a-117">-Confirm</span></span>
<span data-ttu-id="3318a-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3318a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3318a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3318a-119">-DefaultProfile</span></span>
<span data-ttu-id="3318a-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3318a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3318a-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="3318a-121">-DiskId</span></span>
<span data-ttu-id="3318a-122">指定受管理的磁片識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="3318a-122">Specifies the list of managed disk Ids.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3318a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3318a-123">-InputObject</span></span>
<span data-ttu-id="3318a-124">Cmdlet 的輸入物件：與要移除之磁片對應的 ASR 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="3318a-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3318a-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="3318a-125">-VhdUri</span></span>
<span data-ttu-id="3318a-126">指定 vhd Uri 的清單。</span><span class="sxs-lookup"><span data-stu-id="3318a-126">Specifies the list of vhd Uri's.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3318a-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="3318a-127">-WaitForCompletion</span></span>
<span data-ttu-id="3318a-128">等待完成</span><span class="sxs-lookup"><span data-stu-id="3318a-128">Wait For Completion</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3318a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3318a-129">-WhatIf</span></span>
<span data-ttu-id="3318a-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3318a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3318a-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3318a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3318a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3318a-132">CommonParameters</span></span>
<span data-ttu-id="3318a-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3318a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3318a-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3318a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3318a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="3318a-135">INPUTS</span></span>

### <span data-ttu-id="3318a-136">RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3318a-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="3318a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3318a-137">OUTPUTS</span></span>

### <span data-ttu-id="3318a-138">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3318a-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3318a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3318a-139">NOTES</span></span>

## <span data-ttu-id="3318a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="3318a-140">RELATED LINKS</span></span>
