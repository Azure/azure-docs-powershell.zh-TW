---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a51be31c510d7e428ced0c9ce5ab73a80ab28f75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446064"
---
# <span data-ttu-id="c2787-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c2787-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="c2787-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2787-102">SYNOPSIS</span></span>
<span data-ttu-id="c2787-103">從 [恢復服務] 保存庫刪除指定的 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="c2787-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2787-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2787-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2787-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2787-105">DESCRIPTION</span></span>
<span data-ttu-id="c2787-106">**AzureRmRecoveryServicesAsrNetworkMapping** Cmdlet 會刪除指定的 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="c2787-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="c2787-107">示例</span><span class="sxs-lookup"><span data-stu-id="c2787-107">EXAMPLES</span></span>

### <span data-ttu-id="c2787-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c2787-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="c2787-109">開始刪除指定的 ASR 網路對應，並傳回用於追蹤操作的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="c2787-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c2787-110">參數</span><span class="sxs-lookup"><span data-stu-id="c2787-110">PARAMETERS</span></span>

### <span data-ttu-id="c2787-111">-確認</span><span class="sxs-lookup"><span data-stu-id="c2787-111">-Confirm</span></span>
<span data-ttu-id="c2787-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c2787-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2787-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2787-113">-DefaultProfile</span></span>
<span data-ttu-id="c2787-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2787-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2787-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2787-115">-InputObject</span></span>
<span data-ttu-id="c2787-116">Cmdlet 的輸入物件：與要刪除之 ASR 網路對應的 ASR 網路對應物件。</span><span class="sxs-lookup"><span data-stu-id="c2787-116">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2787-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2787-117">-WhatIf</span></span>
<span data-ttu-id="c2787-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2787-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2787-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2787-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2787-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2787-120">CommonParameters</span></span>
<span data-ttu-id="c2787-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2787-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2787-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2787-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2787-123">輸入</span><span class="sxs-lookup"><span data-stu-id="c2787-123">INPUTS</span></span>

### <span data-ttu-id="c2787-124">RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c2787-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="c2787-125">輸出</span><span class="sxs-lookup"><span data-stu-id="c2787-125">OUTPUTS</span></span>

### <span data-ttu-id="c2787-126">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c2787-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c2787-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c2787-127">NOTES</span></span>

## <span data-ttu-id="c2787-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2787-128">RELATED LINKS</span></span>

[<span data-ttu-id="c2787-129">AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c2787-129">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="c2787-130">新-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="c2787-130">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
