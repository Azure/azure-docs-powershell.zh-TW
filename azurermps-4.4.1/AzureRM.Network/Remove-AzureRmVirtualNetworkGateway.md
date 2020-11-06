---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 401fcbd5fca9fc0251e4de0fb7843fb95c1c122d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454299"
---
# <span data-ttu-id="d990a-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d990a-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="d990a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d990a-102">SYNOPSIS</span></span>
<span data-ttu-id="d990a-103">刪除虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="d990a-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d990a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d990a-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d990a-105">說明</span><span class="sxs-lookup"><span data-stu-id="d990a-105">DESCRIPTION</span></span>
<span data-ttu-id="d990a-106">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="d990a-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="d990a-107">**AzureRmVirtualNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，傳回 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="d990a-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="d990a-108">示例</span><span class="sxs-lookup"><span data-stu-id="d990a-108">EXAMPLES</span></span>

### <span data-ttu-id="d990a-109">1：刪除虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="d990a-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="d990a-110">刪除資源群組 "myRG" 中名稱為 "myGateway" 的虛擬網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="d990a-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="d990a-111">注意：您必須先使用 **AzureRmVirtualNetworkGatewayConnection** Cmdlet 刪除所有連線至虛擬網路閘道的連線。</span><span class="sxs-lookup"><span data-stu-id="d990a-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="d990a-112">參數</span><span class="sxs-lookup"><span data-stu-id="d990a-112">PARAMETERS</span></span>

### <span data-ttu-id="d990a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d990a-113">-Force</span></span>
<span data-ttu-id="d990a-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d990a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d990a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d990a-115">-Name</span></span>
<span data-ttu-id="d990a-116">指定此 Cmdlet 移除之虛擬網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="d990a-116">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d990a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d990a-117">-PassThru</span></span>
<span data-ttu-id="d990a-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d990a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d990a-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d990a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d990a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d990a-120">-ResourceGroupName</span></span>
<span data-ttu-id="d990a-121">指定包含虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d990a-121">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d990a-122">-確認</span><span class="sxs-lookup"><span data-stu-id="d990a-122">-Confirm</span></span>
<span data-ttu-id="d990a-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d990a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d990a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d990a-124">-WhatIf</span></span>
<span data-ttu-id="d990a-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d990a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d990a-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d990a-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d990a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d990a-127">-DefaultProfile</span></span>
<span data-ttu-id="d990a-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d990a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d990a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d990a-129">CommonParameters</span></span>
<span data-ttu-id="d990a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d990a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d990a-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d990a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d990a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d990a-132">INPUTS</span></span>

## <span data-ttu-id="d990a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d990a-133">OUTPUTS</span></span>

## <span data-ttu-id="d990a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d990a-134">NOTES</span></span>

## <span data-ttu-id="d990a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d990a-135">RELATED LINKS</span></span>

