---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 095759ca2753cac4f7155430a241e0554e910fd6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958585"
---
# <span data-ttu-id="09337-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="09337-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="09337-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09337-102">SYNOPSIS</span></span>
<span data-ttu-id="09337-103">從 [恢復服務] 保存庫刪除指定的 Azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="09337-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="09337-104">句法</span><span class="sxs-lookup"><span data-stu-id="09337-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09337-105">說明</span><span class="sxs-lookup"><span data-stu-id="09337-105">DESCRIPTION</span></span>
<span data-ttu-id="09337-106">**AzRecoveryServicesAsrFabric** Cmdlet 會從 [恢復服務] 保存庫中移除指定的 Azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="09337-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="09337-107">示例</span><span class="sxs-lookup"><span data-stu-id="09337-107">EXAMPLES</span></span>

### <span data-ttu-id="09337-108">範例1</span><span class="sxs-lookup"><span data-stu-id="09337-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="09337-109">開始刪除指定的結構，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="09337-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="09337-110">參數</span><span class="sxs-lookup"><span data-stu-id="09337-110">PARAMETERS</span></span>

### <span data-ttu-id="09337-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09337-111">-DefaultProfile</span></span>
<span data-ttu-id="09337-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="09337-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="09337-113">-Force</span><span class="sxs-lookup"><span data-stu-id="09337-113">-Force</span></span>
<span data-ttu-id="09337-114">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="09337-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="09337-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09337-115">-InputObject</span></span>
<span data-ttu-id="09337-116">Cmdlet 的輸入物件：對應到要刪除之結構的 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="09337-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="09337-117">-確認</span><span class="sxs-lookup"><span data-stu-id="09337-117">-Confirm</span></span>
<span data-ttu-id="09337-118">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="09337-118">Specify if confirmation is required.</span></span> <span data-ttu-id="09337-119">將確認參數的值設定為 [$false]，以略過確認。</span><span class="sxs-lookup"><span data-stu-id="09337-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="09337-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09337-120">-WhatIf</span></span>
<span data-ttu-id="09337-121">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09337-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="09337-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09337-122">CommonParameters</span></span>
<span data-ttu-id="09337-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09337-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09337-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="09337-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09337-125">輸入</span><span class="sxs-lookup"><span data-stu-id="09337-125">INPUTS</span></span>

### <span data-ttu-id="09337-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="09337-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="09337-127">輸出</span><span class="sxs-lookup"><span data-stu-id="09337-127">OUTPUTS</span></span>

### <span data-ttu-id="09337-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="09337-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="09337-129">筆記</span><span class="sxs-lookup"><span data-stu-id="09337-129">NOTES</span></span>

## <span data-ttu-id="09337-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="09337-130">RELATED LINKS</span></span>

[<span data-ttu-id="09337-131">AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="09337-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="09337-132">新-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="09337-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
