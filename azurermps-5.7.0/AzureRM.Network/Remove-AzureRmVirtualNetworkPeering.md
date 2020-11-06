---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkPeering.md
ms.openlocfilehash: a128f7c9e9440255ed01b32c4460ffd180655928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456175"
---
# <span data-ttu-id="eb9d9-101">Remove-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="eb9d9-101">Remove-AzureRmVirtualNetworkPeering</span></span>

## <span data-ttu-id="eb9d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb9d9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb9d9-103">句法</span><span class="sxs-lookup"><span data-stu-id="eb9d9-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb9d9-104">說明</span><span class="sxs-lookup"><span data-stu-id="eb9d9-104">DESCRIPTION</span></span>

## <span data-ttu-id="eb9d9-105">示例</span><span class="sxs-lookup"><span data-stu-id="eb9d9-105">EXAMPLES</span></span>

### <span data-ttu-id="eb9d9-106">範例1：移除虛擬網路對等</span><span class="sxs-lookup"><span data-stu-id="eb9d9-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzureRmVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="eb9d9-107">參數</span><span class="sxs-lookup"><span data-stu-id="eb9d9-107">PARAMETERS</span></span>

### <span data-ttu-id="eb9d9-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb9d9-108">-AsJob</span></span>
<span data-ttu-id="eb9d9-109">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eb9d9-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb9d9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb9d9-110">-DefaultProfile</span></span>
<span data-ttu-id="eb9d9-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb9d9-112">-Force</span><span class="sxs-lookup"><span data-stu-id="eb9d9-112">-Force</span></span>
<span data-ttu-id="eb9d9-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eb9d9-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb9d9-114">-Name</span></span>
<span data-ttu-id="eb9d9-115">虛擬網路對等名稱。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-115">The virtual network peering name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9d9-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb9d9-116">-PassThru</span></span>
<span data-ttu-id="eb9d9-117">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eb9d9-118">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eb9d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb9d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="eb9d9-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="eb9d9-120">The resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9d9-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="eb9d9-121">-VirtualNetworkName</span></span>
<span data-ttu-id="eb9d9-122">虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-122">The virtual network name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb9d9-123">-確認</span><span class="sxs-lookup"><span data-stu-id="eb9d9-123">-Confirm</span></span>
<span data-ttu-id="eb9d9-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9d9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb9d9-125">-WhatIf</span></span>
<span data-ttu-id="eb9d9-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb9d9-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb9d9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb9d9-128">CommonParameters</span></span>
<span data-ttu-id="eb9d9-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb9d9-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb9d9-131">輸入</span><span class="sxs-lookup"><span data-stu-id="eb9d9-131">INPUTS</span></span>

### <span data-ttu-id="eb9d9-132">所有</span><span class="sxs-lookup"><span data-stu-id="eb9d9-132">None</span></span>
<span data-ttu-id="eb9d9-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="eb9d9-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb9d9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="eb9d9-134">OUTPUTS</span></span>

## <span data-ttu-id="eb9d9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="eb9d9-135">NOTES</span></span>

## <span data-ttu-id="eb9d9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb9d9-136">RELATED LINKS</span></span>

