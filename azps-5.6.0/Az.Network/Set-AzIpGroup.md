---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 8f8e40f5b2209b75c52376c08b69dff8946add77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908054"
---
# <span data-ttu-id="decb5-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="decb5-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="decb5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="decb5-102">SYNOPSIS</span></span>
<span data-ttu-id="decb5-103">會保存已修改的防火牆。</span><span class="sxs-lookup"><span data-stu-id="decb5-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="decb5-104">語法</span><span class="sxs-lookup"><span data-stu-id="decb5-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="decb5-105">描述</span><span class="sxs-lookup"><span data-stu-id="decb5-105">DESCRIPTION</span></span>
<span data-ttu-id="decb5-106">**Set-AzIpGroup** Cmdlet 會更新 Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="decb5-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="decb5-107">例子</span><span class="sxs-lookup"><span data-stu-id="decb5-107">EXAMPLES</span></span>

### <span data-ttu-id="decb5-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="decb5-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="decb5-109">參數</span><span class="sxs-lookup"><span data-stu-id="decb5-109">PARAMETERS</span></span>

### <span data-ttu-id="decb5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="decb5-110">-AsJob</span></span>
<span data-ttu-id="decb5-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="decb5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="decb5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="decb5-112">-DefaultProfile</span></span>
<span data-ttu-id="decb5-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="decb5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="decb5-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="decb5-114">-IpGroup</span></span>
<span data-ttu-id="decb5-115">The IpGroup</span><span class="sxs-lookup"><span data-stu-id="decb5-115">The IpGroup</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="decb5-116">-確認</span><span class="sxs-lookup"><span data-stu-id="decb5-116">-Confirm</span></span>
<span data-ttu-id="decb5-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="decb5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="decb5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="decb5-118">-WhatIf</span></span>
<span data-ttu-id="decb5-119">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="decb5-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="decb5-120">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="decb5-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="decb5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decb5-121">CommonParameters</span></span>
<span data-ttu-id="decb5-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="decb5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decb5-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="decb5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decb5-124">輸入</span><span class="sxs-lookup"><span data-stu-id="decb5-124">INPUTS</span></span>

### <span data-ttu-id="decb5-125">Microsoft.Azure.Commands.Network.models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="decb5-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="decb5-126">輸出</span><span class="sxs-lookup"><span data-stu-id="decb5-126">OUTPUTS</span></span>

### <span data-ttu-id="decb5-127">Microsoft.Azure.Commands.Network.models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="decb5-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="decb5-128">筆記</span><span class="sxs-lookup"><span data-stu-id="decb5-128">NOTES</span></span>

## <span data-ttu-id="decb5-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="decb5-129">RELATED LINKS</span></span>
