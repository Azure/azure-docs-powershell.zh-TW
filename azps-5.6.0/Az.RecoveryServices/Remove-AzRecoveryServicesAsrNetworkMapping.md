---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: bb80bebc8c1a5dccbeedf4abd277891c3b2e9de7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902242"
---
# <span data-ttu-id="a1e5b-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a1e5b-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="a1e5b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e5b-103">從修復服務儲存庫刪除指定的 ASR 網路地圖。</span><span class="sxs-lookup"><span data-stu-id="a1e5b-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="a1e5b-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1e5b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1e5b-105">描述</span><span class="sxs-lookup"><span data-stu-id="a1e5b-105">DESCRIPTION</span></span>
<span data-ttu-id="a1e5b-106">**Remove-AzRecoveryServicesAsrNetworkMapping** Cmdlet 會刪除指定的 ASR 網路地圖。</span><span class="sxs-lookup"><span data-stu-id="a1e5b-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="a1e5b-107">例子</span><span class="sxs-lookup"><span data-stu-id="a1e5b-107">EXAMPLES</span></span>

### <span data-ttu-id="a1e5b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a1e5b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="a1e5b-109">開始刪除指定的 ASR 網路映射，並返回用來追蹤作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="a1e5b-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a1e5b-110">參數</span><span class="sxs-lookup"><span data-stu-id="a1e5b-110">PARAMETERS</span></span>

### <span data-ttu-id="a1e5b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e5b-111">-DefaultProfile</span></span>
<span data-ttu-id="a1e5b-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1e5b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a1e5b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1e5b-113">-InputObject</span></span>
<span data-ttu-id="a1e5b-114">Cmdlet 的輸入物件：對應至要刪除之 ASR 網路對應的 ASR 網路對應物件。</span><span class="sxs-lookup"><span data-stu-id="a1e5b-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e5b-115">-確認</span><span class="sxs-lookup"><span data-stu-id="a1e5b-115">-Confirm</span></span>
<span data-ttu-id="a1e5b-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a1e5b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1e5b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1e5b-117">-WhatIf</span></span>
<span data-ttu-id="a1e5b-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1e5b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1e5b-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1e5b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1e5b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e5b-120">CommonParameters</span></span>
<span data-ttu-id="a1e5b-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1e5b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e5b-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1e5b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e5b-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a1e5b-123">INPUTS</span></span>

### <span data-ttu-id="a1e5b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a1e5b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="a1e5b-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a1e5b-125">OUTPUTS</span></span>

### <span data-ttu-id="a1e5b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a1e5b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a1e5b-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a1e5b-127">NOTES</span></span>

## <span data-ttu-id="a1e5b-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1e5b-128">RELATED LINKS</span></span>

[<span data-ttu-id="a1e5b-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a1e5b-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="a1e5b-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a1e5b-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
