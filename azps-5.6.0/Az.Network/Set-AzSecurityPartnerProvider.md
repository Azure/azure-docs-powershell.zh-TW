---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzSecurityPartnerProvider.md
ms.openlocfilehash: 0a9ed100121c0f6610bcb019571fd1779f28dff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916714"
---
# <span data-ttu-id="dbf81-101">Set-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="dbf81-101">Set-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="dbf81-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dbf81-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf81-103">會預存已修改的 Azure SecurityPartnerProvider。</span><span class="sxs-lookup"><span data-stu-id="dbf81-103">Saves a modified Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="dbf81-104">語法</span><span class="sxs-lookup"><span data-stu-id="dbf81-104">SYNTAX</span></span>

```
Set-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbf81-105">描述</span><span class="sxs-lookup"><span data-stu-id="dbf81-105">DESCRIPTION</span></span>
<span data-ttu-id="dbf81-106">**Set-AzSecurityPartnerProvider Cmdlet** 會更新 Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="dbf81-106">The **Set-AzSecurityPartnerProvider** cmdlet updates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="dbf81-107">例子</span><span class="sxs-lookup"><span data-stu-id="dbf81-107">EXAMPLES</span></span>

### <span data-ttu-id="dbf81-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="dbf81-108">Example 1</span></span>
```powershell
$securityPartnerProvider = Get-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
Set-AzSecurityPartnerProvider -SecurityPartnerProvider $securityPartnerProvider
```


## <span data-ttu-id="dbf81-109">參數</span><span class="sxs-lookup"><span data-stu-id="dbf81-109">PARAMETERS</span></span>

### <span data-ttu-id="dbf81-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbf81-110">-AsJob</span></span>
<span data-ttu-id="dbf81-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dbf81-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf81-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf81-112">-DefaultProfile</span></span>
<span data-ttu-id="dbf81-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbf81-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf81-114">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="dbf81-114">-SecurityPartnerProvider</span></span>
<span data-ttu-id="dbf81-115">The SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="dbf81-115">The SecurityPartnerProvider</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbf81-116">-確認</span><span class="sxs-lookup"><span data-stu-id="dbf81-116">-Confirm</span></span>
<span data-ttu-id="dbf81-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dbf81-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf81-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf81-118">-WhatIf</span></span>
<span data-ttu-id="dbf81-119">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbf81-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbf81-120">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbf81-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf81-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf81-121">CommonParameters</span></span>
<span data-ttu-id="dbf81-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dbf81-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf81-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbf81-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf81-124">輸入</span><span class="sxs-lookup"><span data-stu-id="dbf81-124">INPUTS</span></span>

### <span data-ttu-id="dbf81-125">Microsoft.Azure.Commands.Network.models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="dbf81-125">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="dbf81-126">輸出</span><span class="sxs-lookup"><span data-stu-id="dbf81-126">OUTPUTS</span></span>

### <span data-ttu-id="dbf81-127">Microsoft.Azure.Commands.Network.models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="dbf81-127">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="dbf81-128">筆記</span><span class="sxs-lookup"><span data-stu-id="dbf81-128">NOTES</span></span>

## <span data-ttu-id="dbf81-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbf81-129">RELATED LINKS</span></span>
