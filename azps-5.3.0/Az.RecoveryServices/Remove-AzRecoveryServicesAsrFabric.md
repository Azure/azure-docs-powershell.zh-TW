---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 095759ca2753cac4f7155430a241e0554e910fd6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437276"
---
# <span data-ttu-id="40968-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="40968-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="40968-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40968-102">SYNOPSIS</span></span>
<span data-ttu-id="40968-103">從 [恢復服務] 保存庫刪除指定的 Azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="40968-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="40968-104">句法</span><span class="sxs-lookup"><span data-stu-id="40968-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40968-105">說明</span><span class="sxs-lookup"><span data-stu-id="40968-105">DESCRIPTION</span></span>
<span data-ttu-id="40968-106">**AzRecoveryServicesAsrFabric** Cmdlet 會從 [恢復服務] 保存庫中移除指定的 Azure 網站復原結構。</span><span class="sxs-lookup"><span data-stu-id="40968-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="40968-107">示例</span><span class="sxs-lookup"><span data-stu-id="40968-107">EXAMPLES</span></span>

### <span data-ttu-id="40968-108">範例1</span><span class="sxs-lookup"><span data-stu-id="40968-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="40968-109">開始刪除指定的結構，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="40968-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="40968-110">參數</span><span class="sxs-lookup"><span data-stu-id="40968-110">PARAMETERS</span></span>

### <span data-ttu-id="40968-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40968-111">-DefaultProfile</span></span>
<span data-ttu-id="40968-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40968-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="40968-113">-Force</span><span class="sxs-lookup"><span data-stu-id="40968-113">-Force</span></span>
<span data-ttu-id="40968-114">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="40968-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="40968-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40968-115">-InputObject</span></span>
<span data-ttu-id="40968-116">Cmdlet 的輸入物件：對應到要刪除之結構的 ASR fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="40968-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="40968-117">-確認</span><span class="sxs-lookup"><span data-stu-id="40968-117">-Confirm</span></span>
<span data-ttu-id="40968-118">指定是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="40968-118">Specify if confirmation is required.</span></span> <span data-ttu-id="40968-119">將確認參數的值設定為 [$false]，以略過確認。</span><span class="sxs-lookup"><span data-stu-id="40968-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="40968-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40968-120">-WhatIf</span></span>
<span data-ttu-id="40968-121">顯示在未實際執行 Cmdlet 的情況下執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40968-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="40968-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40968-122">CommonParameters</span></span>
<span data-ttu-id="40968-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40968-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40968-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="40968-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40968-125">輸入</span><span class="sxs-lookup"><span data-stu-id="40968-125">INPUTS</span></span>

### <span data-ttu-id="40968-126">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="40968-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="40968-127">輸出</span><span class="sxs-lookup"><span data-stu-id="40968-127">OUTPUTS</span></span>

### <span data-ttu-id="40968-128">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="40968-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="40968-129">筆記</span><span class="sxs-lookup"><span data-stu-id="40968-129">NOTES</span></span>

## <span data-ttu-id="40968-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="40968-130">RELATED LINKS</span></span>

[<span data-ttu-id="40968-131">AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="40968-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="40968-132">新-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="40968-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
