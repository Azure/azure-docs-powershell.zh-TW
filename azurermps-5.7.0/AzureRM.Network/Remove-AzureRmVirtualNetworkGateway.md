---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 533eb9482c2e872c0b41552a5c59842a07fa0216
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626142"
---
# <span data-ttu-id="1f03f-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1f03f-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="1f03f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f03f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f03f-103">刪除虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="1f03f-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f03f-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f03f-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f03f-105">說明</span><span class="sxs-lookup"><span data-stu-id="1f03f-105">DESCRIPTION</span></span>
<span data-ttu-id="1f03f-106">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="1f03f-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="1f03f-107">**AzureRmVirtualNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，傳回 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="1f03f-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="1f03f-108">示例</span><span class="sxs-lookup"><span data-stu-id="1f03f-108">EXAMPLES</span></span>

### <span data-ttu-id="1f03f-109">1：刪除虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="1f03f-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="1f03f-110">刪除資源群組 "myRG" 中名稱為 "myGateway" 的虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="1f03f-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="1f03f-111">注意：您必須先使用 **AzureRmVirtualNetworkGatewayConnection** Cmdlet 刪除所有連線至虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="1f03f-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="1f03f-112">參數</span><span class="sxs-lookup"><span data-stu-id="1f03f-112">PARAMETERS</span></span>

### <span data-ttu-id="1f03f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f03f-113">-AsJob</span></span>
<span data-ttu-id="1f03f-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1f03f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f03f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f03f-115">-DefaultProfile</span></span>
<span data-ttu-id="1f03f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f03f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f03f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1f03f-117">-Force</span></span>
<span data-ttu-id="1f03f-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1f03f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f03f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f03f-119">-Name</span></span>
<span data-ttu-id="1f03f-120">指定此 Cmdlet 移除之虛擬網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f03f-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f03f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f03f-121">-PassThru</span></span>
<span data-ttu-id="1f03f-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="1f03f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f03f-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="1f03f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f03f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f03f-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f03f-125">指定包含虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f03f-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="1f03f-126">-確認</span><span class="sxs-lookup"><span data-stu-id="1f03f-126">-Confirm</span></span>
<span data-ttu-id="1f03f-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f03f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f03f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f03f-128">-WhatIf</span></span>
<span data-ttu-id="1f03f-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f03f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f03f-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f03f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f03f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f03f-131">CommonParameters</span></span>
<span data-ttu-id="1f03f-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f03f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f03f-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f03f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f03f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="1f03f-134">INPUTS</span></span>

### <span data-ttu-id="1f03f-135">所有</span><span class="sxs-lookup"><span data-stu-id="1f03f-135">None</span></span>
<span data-ttu-id="1f03f-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1f03f-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f03f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1f03f-137">OUTPUTS</span></span>

## <span data-ttu-id="1f03f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="1f03f-138">NOTES</span></span>

## <span data-ttu-id="1f03f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f03f-139">RELATED LINKS</span></span>

