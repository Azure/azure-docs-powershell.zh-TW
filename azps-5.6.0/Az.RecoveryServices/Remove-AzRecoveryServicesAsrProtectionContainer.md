---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: c1b5623e185c10471da674c21995917c169e5ffa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902237"
---
# <span data-ttu-id="43567-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="43567-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="43567-102">簡介</span><span class="sxs-lookup"><span data-stu-id="43567-102">SYNOPSIS</span></span>
<span data-ttu-id="43567-103">從布藝中刪除指定的保護容器。</span><span class="sxs-lookup"><span data-stu-id="43567-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="43567-104">語法</span><span class="sxs-lookup"><span data-stu-id="43567-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43567-105">描述</span><span class="sxs-lookup"><span data-stu-id="43567-105">DESCRIPTION</span></span>
<span data-ttu-id="43567-106">Cmdlet Remove-AzRecoveryServicesAsrProtectionContainer刪除指定的 Azure 網站復原保護容器。</span><span class="sxs-lookup"><span data-stu-id="43567-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="43567-107">例子</span><span class="sxs-lookup"><span data-stu-id="43567-107">EXAMPLES</span></span>

### <span data-ttu-id="43567-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="43567-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="43567-109">開始刪除指定的保護容器，並返回用來追蹤移除作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="43567-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="43567-110">參數</span><span class="sxs-lookup"><span data-stu-id="43567-110">PARAMETERS</span></span>

### <span data-ttu-id="43567-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43567-111">-DefaultProfile</span></span>
<span data-ttu-id="43567-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="43567-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43567-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43567-113">-InputObject</span></span>
<span data-ttu-id="43567-114">指定要移除的保護容器。</span><span class="sxs-lookup"><span data-stu-id="43567-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="43567-115">-確認</span><span class="sxs-lookup"><span data-stu-id="43567-115">-Confirm</span></span>
<span data-ttu-id="43567-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="43567-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43567-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43567-117">-WhatIf</span></span>
<span data-ttu-id="43567-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43567-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43567-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43567-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43567-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43567-120">CommonParameters</span></span>
<span data-ttu-id="43567-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="43567-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43567-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43567-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43567-123">輸入</span><span class="sxs-lookup"><span data-stu-id="43567-123">INPUTS</span></span>

### <span data-ttu-id="43567-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="43567-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="43567-125">輸出</span><span class="sxs-lookup"><span data-stu-id="43567-125">OUTPUTS</span></span>

### <span data-ttu-id="43567-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="43567-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="43567-127">筆記</span><span class="sxs-lookup"><span data-stu-id="43567-127">NOTES</span></span>

## <span data-ttu-id="43567-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="43567-128">RELATED LINKS</span></span>
