---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzIpGroup.md
ms.openlocfilehash: 2d78e7136fe42187cbabc2345e2ad2314af1d9c5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278510"
---
# <span data-ttu-id="c31ae-101">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="c31ae-101">Set-AzIpGroup</span></span>

## <span data-ttu-id="c31ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c31ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c31ae-103">儲存已修改的防火牆。</span><span class="sxs-lookup"><span data-stu-id="c31ae-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="c31ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="c31ae-104">SYNTAX</span></span>

```
Set-AzIpGroup -IpGroup <PSIpGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c31ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="c31ae-105">DESCRIPTION</span></span>
<span data-ttu-id="c31ae-106">**AzIpGroup** Cmdlet 會更新 Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="c31ae-106">The **Set-AzIpGroup** cmdlet updates an Azure IpGroup</span></span>

## <span data-ttu-id="c31ae-107">示例</span><span class="sxs-lookup"><span data-stu-id="c31ae-107">EXAMPLES</span></span>

### <span data-ttu-id="c31ae-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c31ae-108">Example 1</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
$ipGroup.IpAddresses.Add("11.11.0.0/24")
Set-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="c31ae-109">參數</span><span class="sxs-lookup"><span data-stu-id="c31ae-109">PARAMETERS</span></span>

### <span data-ttu-id="c31ae-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c31ae-110">-AsJob</span></span>
<span data-ttu-id="c31ae-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c31ae-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c31ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c31ae-112">-DefaultProfile</span></span>
<span data-ttu-id="c31ae-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c31ae-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c31ae-114">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="c31ae-114">-IpGroup</span></span>
<span data-ttu-id="c31ae-115">IpGroup</span><span class="sxs-lookup"><span data-stu-id="c31ae-115">The IpGroup</span></span>

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

### <span data-ttu-id="c31ae-116">-確認</span><span class="sxs-lookup"><span data-stu-id="c31ae-116">-Confirm</span></span>
<span data-ttu-id="c31ae-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c31ae-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c31ae-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c31ae-118">-WhatIf</span></span>
<span data-ttu-id="c31ae-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c31ae-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c31ae-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c31ae-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c31ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c31ae-121">CommonParameters</span></span>
<span data-ttu-id="c31ae-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c31ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c31ae-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c31ae-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c31ae-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c31ae-124">INPUTS</span></span>

### <span data-ttu-id="c31ae-125">PSIpGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c31ae-125">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="c31ae-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c31ae-126">OUTPUTS</span></span>

### <span data-ttu-id="c31ae-127">PSIpGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c31ae-127">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="c31ae-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c31ae-128">NOTES</span></span>

## <span data-ttu-id="c31ae-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c31ae-129">RELATED LINKS</span></span>
