---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139487"
---
# <span data-ttu-id="5e234-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5e234-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="5e234-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e234-102">SYNOPSIS</span></span>
<span data-ttu-id="5e234-103">從其結構中刪除指定的保護容器。</span><span class="sxs-lookup"><span data-stu-id="5e234-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="5e234-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e234-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e234-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e234-105">DESCRIPTION</span></span>
<span data-ttu-id="5e234-106">Remove-AzRecoveryServicesAsrProtectionContainer Cmdlet 會刪除指定的 Azure Site Recovery 防護容器。</span><span class="sxs-lookup"><span data-stu-id="5e234-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="5e234-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e234-107">EXAMPLES</span></span>

### <span data-ttu-id="5e234-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5e234-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="5e234-109">開始刪除指定的保護容器，並傳回用於追蹤移除操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="5e234-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="5e234-110">參數</span><span class="sxs-lookup"><span data-stu-id="5e234-110">PARAMETERS</span></span>

### <span data-ttu-id="5e234-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e234-111">-DefaultProfile</span></span>
<span data-ttu-id="5e234-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e234-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e234-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e234-113">-InputObject</span></span>
<span data-ttu-id="5e234-114">指定要移除的保護容器。</span><span class="sxs-lookup"><span data-stu-id="5e234-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e234-115">-確認</span><span class="sxs-lookup"><span data-stu-id="5e234-115">-Confirm</span></span>
<span data-ttu-id="5e234-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5e234-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e234-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e234-117">-WhatIf</span></span>
<span data-ttu-id="5e234-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e234-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e234-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e234-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e234-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e234-120">CommonParameters</span></span>
<span data-ttu-id="5e234-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e234-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e234-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5e234-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e234-123">輸入</span><span class="sxs-lookup"><span data-stu-id="5e234-123">INPUTS</span></span>

### <span data-ttu-id="5e234-124">RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5e234-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="5e234-125">輸出</span><span class="sxs-lookup"><span data-stu-id="5e234-125">OUTPUTS</span></span>

### <span data-ttu-id="5e234-126">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5e234-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5e234-127">筆記</span><span class="sxs-lookup"><span data-stu-id="5e234-127">NOTES</span></span>

## <span data-ttu-id="5e234-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e234-128">RELATED LINKS</span></span>