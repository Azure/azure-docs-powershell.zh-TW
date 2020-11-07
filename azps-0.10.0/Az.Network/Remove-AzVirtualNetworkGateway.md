---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: bb63f9d56dc78943f9232107e39188ae3d29f43f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795485"
---
# <span data-ttu-id="6f410-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6f410-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="6f410-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f410-102">SYNOPSIS</span></span>
<span data-ttu-id="6f410-103">刪除虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="6f410-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="6f410-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f410-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f410-105">說明</span><span class="sxs-lookup"><span data-stu-id="6f410-105">DESCRIPTION</span></span>
<span data-ttu-id="6f410-106">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="6f410-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="6f410-107">**AzVirtualNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，傳回 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="6f410-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="6f410-108">示例</span><span class="sxs-lookup"><span data-stu-id="6f410-108">EXAMPLES</span></span>

### <span data-ttu-id="6f410-109">1：刪除虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="6f410-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="6f410-110">刪除資源群組 "myRG" 中名稱為 "myGateway" 的虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="6f410-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="6f410-111">注意：您必須先使用 **AzVirtualNetworkGatewayConnection** Cmdlet 刪除所有連線至虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="6f410-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="6f410-112">參數</span><span class="sxs-lookup"><span data-stu-id="6f410-112">PARAMETERS</span></span>

### <span data-ttu-id="6f410-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f410-113">-AsJob</span></span>
<span data-ttu-id="6f410-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6f410-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f410-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f410-115">-DefaultProfile</span></span>
<span data-ttu-id="6f410-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f410-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f410-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6f410-117">-Force</span></span>
<span data-ttu-id="6f410-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6f410-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f410-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f410-119">-Name</span></span>
<span data-ttu-id="6f410-120">指定此 Cmdlet 移除之虛擬網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f410-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6f410-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f410-121">-PassThru</span></span>
<span data-ttu-id="6f410-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="6f410-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6f410-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6f410-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6f410-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f410-124">-ResourceGroupName</span></span>
<span data-ttu-id="6f410-125">指定包含虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f410-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="6f410-126">-確認</span><span class="sxs-lookup"><span data-stu-id="6f410-126">-Confirm</span></span>
<span data-ttu-id="6f410-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f410-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f410-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f410-128">-WhatIf</span></span>
<span data-ttu-id="6f410-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f410-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f410-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f410-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f410-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f410-131">CommonParameters</span></span>
<span data-ttu-id="6f410-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f410-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f410-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f410-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f410-134">輸入</span><span class="sxs-lookup"><span data-stu-id="6f410-134">INPUTS</span></span>

## <span data-ttu-id="6f410-135">輸出</span><span class="sxs-lookup"><span data-stu-id="6f410-135">OUTPUTS</span></span>

## <span data-ttu-id="6f410-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6f410-136">NOTES</span></span>

## <span data-ttu-id="6f410-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f410-137">RELATED LINKS</span></span>

