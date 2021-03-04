---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f7d71d0e69f83633d02832bd3f54554be1fa0ba0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902234"
---
# <span data-ttu-id="88bf3-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="88bf3-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="88bf3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="88bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="88bf3-103">刪除指定的 Azure 網站復原保護容器映射。</span><span class="sxs-lookup"><span data-stu-id="88bf3-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="88bf3-104">語法</span><span class="sxs-lookup"><span data-stu-id="88bf3-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88bf3-105">描述</span><span class="sxs-lookup"><span data-stu-id="88bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="88bf3-106">**Remove-AzRecoveryServicesrProtectionContainerMadlet** 會刪除指定的 Azure 網站復原保護容器地圖。</span><span class="sxs-lookup"><span data-stu-id="88bf3-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="88bf3-107">例子</span><span class="sxs-lookup"><span data-stu-id="88bf3-107">EXAMPLES</span></span>

### <span data-ttu-id="88bf3-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="88bf3-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="88bf3-109">開始刪除指定的保護容器映射，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="88bf3-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="88bf3-110">參數</span><span class="sxs-lookup"><span data-stu-id="88bf3-110">PARAMETERS</span></span>

### <span data-ttu-id="88bf3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88bf3-111">-DefaultProfile</span></span>
<span data-ttu-id="88bf3-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="88bf3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="88bf3-113">-強制</span><span class="sxs-lookup"><span data-stu-id="88bf3-113">-Force</span></span>
<span data-ttu-id="88bf3-114">強制執行命令，但不提供額外的警告。</span><span class="sxs-lookup"><span data-stu-id="88bf3-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="88bf3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88bf3-115">-InputObject</span></span>
<span data-ttu-id="88bf3-116">Cmdlet 的輸入物件：對應到要刪除之保護容器的 ASR 保護容器對應物件。</span><span class="sxs-lookup"><span data-stu-id="88bf3-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88bf3-117">-確認</span><span class="sxs-lookup"><span data-stu-id="88bf3-117">-Confirm</span></span>
<span data-ttu-id="88bf3-118">指定如果需要確認。</span><span class="sxs-lookup"><span data-stu-id="88bf3-118">Specify if confirmation is required.</span></span> <span data-ttu-id="88bf3-119">將確認參數的值設為 $false以略過確認</span><span class="sxs-lookup"><span data-stu-id="88bf3-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="88bf3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88bf3-120">-WhatIf</span></span>
<span data-ttu-id="88bf3-121">顯示執行 Cmdlet 而不實際執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88bf3-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="88bf3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bf3-122">CommonParameters</span></span>
<span data-ttu-id="88bf3-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="88bf3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bf3-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88bf3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bf3-125">輸入</span><span class="sxs-lookup"><span data-stu-id="88bf3-125">INPUTS</span></span>

### <span data-ttu-id="88bf3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="88bf3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="88bf3-127">輸出</span><span class="sxs-lookup"><span data-stu-id="88bf3-127">OUTPUTS</span></span>

### <span data-ttu-id="88bf3-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="88bf3-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="88bf3-129">筆記</span><span class="sxs-lookup"><span data-stu-id="88bf3-129">NOTES</span></span>

## <span data-ttu-id="88bf3-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="88bf3-130">RELATED LINKS</span></span>

[<span data-ttu-id="88bf3-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="88bf3-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="88bf3-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="88bf3-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
