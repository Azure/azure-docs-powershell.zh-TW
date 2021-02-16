---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128518"
---
# <span data-ttu-id="0972d-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="0972d-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="0972d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0972d-102">SYNOPSIS</span></span>
<span data-ttu-id="0972d-103">新增磁片以保護已受保護的 azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0972d-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="0972d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0972d-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0972d-105">說明</span><span class="sxs-lookup"><span data-stu-id="0972d-105">DESCRIPTION</span></span>
<span data-ttu-id="0972d-106">**AzRecoveryServicesAsrReplicationProtectedItemDisk** Cmdlet 會為已受保護的 azure 虛擬機器加入保護磁片。</span><span class="sxs-lookup"><span data-stu-id="0972d-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="0972d-107">示例</span><span class="sxs-lookup"><span data-stu-id="0972d-107">EXAMPLES</span></span>

### <span data-ttu-id="0972d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0972d-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="0972d-109">啟動作業以新增指定的磁片設定以進行保護。</span><span class="sxs-lookup"><span data-stu-id="0972d-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="0972d-110">範例2</span><span class="sxs-lookup"><span data-stu-id="0972d-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="0972d-111">啟動作業以新增指定的磁片設定以進行保護。[管道輸入複製受保護的專案]。</span><span class="sxs-lookup"><span data-stu-id="0972d-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="0972d-112">參數</span><span class="sxs-lookup"><span data-stu-id="0972d-112">PARAMETERS</span></span>

### <span data-ttu-id="0972d-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="0972d-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="0972d-114">指定要用於 Azure 到 Azure 災害復原案例之磁片保護的磁片配置。</span><span class="sxs-lookup"><span data-stu-id="0972d-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0972d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0972d-115">-DefaultProfile</span></span>
<span data-ttu-id="0972d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0972d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0972d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0972d-117">-InputObject</span></span>
<span data-ttu-id="0972d-118">Cmdlet 的輸入物件：與要保護的新磁片相對應的 ASR 複製受保護專案物件。</span><span class="sxs-lookup"><span data-stu-id="0972d-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0972d-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="0972d-119">-WaitForCompletion</span></span>
<span data-ttu-id="0972d-120">等待完成</span><span class="sxs-lookup"><span data-stu-id="0972d-120">Wait For Completion</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0972d-121">-確認</span><span class="sxs-lookup"><span data-stu-id="0972d-121">-Confirm</span></span>
<span data-ttu-id="0972d-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0972d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0972d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0972d-123">-WhatIf</span></span>
<span data-ttu-id="0972d-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0972d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0972d-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0972d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0972d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0972d-126">CommonParameters</span></span>
<span data-ttu-id="0972d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0972d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0972d-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0972d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0972d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0972d-129">INPUTS</span></span>

### <span data-ttu-id="0972d-130">所有</span><span class="sxs-lookup"><span data-stu-id="0972d-130">None</span></span>

## <span data-ttu-id="0972d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0972d-131">OUTPUTS</span></span>

### <span data-ttu-id="0972d-132">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0972d-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0972d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0972d-133">NOTES</span></span>

## <span data-ttu-id="0972d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0972d-134">RELATED LINKS</span></span>
