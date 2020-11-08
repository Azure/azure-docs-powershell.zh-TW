---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969130"
---
# <span data-ttu-id="30b87-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="30b87-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="30b87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30b87-102">SYNOPSIS</span></span>
<span data-ttu-id="30b87-103">從 [恢復服務] 保存庫刪除指定的 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="30b87-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="30b87-104">句法</span><span class="sxs-lookup"><span data-stu-id="30b87-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30b87-105">說明</span><span class="sxs-lookup"><span data-stu-id="30b87-105">DESCRIPTION</span></span>
<span data-ttu-id="30b87-106">**AzRecoveryServicesAsrNetworkMapping** Cmdlet 會刪除指定的 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="30b87-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="30b87-107">示例</span><span class="sxs-lookup"><span data-stu-id="30b87-107">EXAMPLES</span></span>

### <span data-ttu-id="30b87-108">範例1</span><span class="sxs-lookup"><span data-stu-id="30b87-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="30b87-109">開始刪除指定的 ASR 網路對應，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="30b87-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="30b87-110">參數</span><span class="sxs-lookup"><span data-stu-id="30b87-110">PARAMETERS</span></span>

### <span data-ttu-id="30b87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b87-111">-DefaultProfile</span></span>
<span data-ttu-id="30b87-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="30b87-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="30b87-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30b87-113">-InputObject</span></span>
<span data-ttu-id="30b87-114">Cmdlet 的輸入物件：與要刪除之 ASR 網路對應的 ASR 網路對應物件。</span><span class="sxs-lookup"><span data-stu-id="30b87-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="30b87-115">-確認</span><span class="sxs-lookup"><span data-stu-id="30b87-115">-Confirm</span></span>
<span data-ttu-id="30b87-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30b87-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30b87-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30b87-117">-WhatIf</span></span>
<span data-ttu-id="30b87-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30b87-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30b87-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30b87-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30b87-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b87-120">CommonParameters</span></span>
<span data-ttu-id="30b87-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30b87-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30b87-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="30b87-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b87-123">輸入</span><span class="sxs-lookup"><span data-stu-id="30b87-123">INPUTS</span></span>

### <span data-ttu-id="30b87-124">RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="30b87-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="30b87-125">輸出</span><span class="sxs-lookup"><span data-stu-id="30b87-125">OUTPUTS</span></span>

### <span data-ttu-id="30b87-126">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="30b87-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="30b87-127">筆記</span><span class="sxs-lookup"><span data-stu-id="30b87-127">NOTES</span></span>

## <span data-ttu-id="30b87-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="30b87-128">RELATED LINKS</span></span>

[<span data-ttu-id="30b87-129">AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="30b87-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="30b87-130">新-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="30b87-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)