---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: ed06852e2ce0342502d01bd7f5ae17c0c3b8f4e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902245"
---
# <span data-ttu-id="e0c25-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e0c25-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="e0c25-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e0c25-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c25-103">從修復服務儲存庫刪除指定的 Azure 網站修復結構。</span><span class="sxs-lookup"><span data-stu-id="e0c25-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="e0c25-104">語法</span><span class="sxs-lookup"><span data-stu-id="e0c25-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0c25-105">描述</span><span class="sxs-lookup"><span data-stu-id="e0c25-105">DESCRIPTION</span></span>
<span data-ttu-id="e0c25-106">**Remove-AzRecoveryServicesAsrFabric** Cmdlet 會從復原服務庫移除指定的 Azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="e0c25-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="e0c25-107">例子</span><span class="sxs-lookup"><span data-stu-id="e0c25-107">EXAMPLES</span></span>

### <span data-ttu-id="e0c25-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e0c25-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="e0c25-109">開始刪除指定的布料，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="e0c25-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e0c25-110">參數</span><span class="sxs-lookup"><span data-stu-id="e0c25-110">PARAMETERS</span></span>

### <span data-ttu-id="e0c25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c25-111">-DefaultProfile</span></span>
<span data-ttu-id="e0c25-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e0c25-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e0c25-113">-強制</span><span class="sxs-lookup"><span data-stu-id="e0c25-113">-Force</span></span>
<span data-ttu-id="e0c25-114">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="e0c25-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="e0c25-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0c25-115">-InputObject</span></span>
<span data-ttu-id="e0c25-116">Cmdlet 的輸入物件：對應到要刪除之布料的 ASR 布料物件。</span><span class="sxs-lookup"><span data-stu-id="e0c25-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0c25-117">-確認</span><span class="sxs-lookup"><span data-stu-id="e0c25-117">-Confirm</span></span>
<span data-ttu-id="e0c25-118">指定如果需要確認。</span><span class="sxs-lookup"><span data-stu-id="e0c25-118">Specify if confirmation is required.</span></span> <span data-ttu-id="e0c25-119">將確認參數的值設定為$false跳過確認。</span><span class="sxs-lookup"><span data-stu-id="e0c25-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="e0c25-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0c25-120">-WhatIf</span></span>
<span data-ttu-id="e0c25-121">顯示執行 Cmdlet 而不實際執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0c25-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="e0c25-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c25-122">CommonParameters</span></span>
<span data-ttu-id="e0c25-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e0c25-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c25-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0c25-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c25-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e0c25-125">INPUTS</span></span>

### <span data-ttu-id="e0c25-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e0c25-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="e0c25-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e0c25-127">OUTPUTS</span></span>

### <span data-ttu-id="e0c25-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="e0c25-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e0c25-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e0c25-129">NOTES</span></span>

## <span data-ttu-id="e0c25-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0c25-130">RELATED LINKS</span></span>

[<span data-ttu-id="e0c25-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e0c25-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="e0c25-132">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="e0c25-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
