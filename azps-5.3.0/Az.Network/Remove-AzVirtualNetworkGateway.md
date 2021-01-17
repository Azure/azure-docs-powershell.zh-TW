---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7708202630b5c7797d9ec3eda77475c82e1c358a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450173"
---
# <span data-ttu-id="ea621-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea621-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="ea621-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea621-102">SYNOPSIS</span></span>
<span data-ttu-id="ea621-103">刪除虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="ea621-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="ea621-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea621-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea621-105">說明</span><span class="sxs-lookup"><span data-stu-id="ea621-105">DESCRIPTION</span></span>
<span data-ttu-id="ea621-106">虛擬網路閘道是代表您在 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="ea621-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="ea621-107">**AzVirtualNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，傳回 Azure 中閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="ea621-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ea621-108">示例</span><span class="sxs-lookup"><span data-stu-id="ea621-108">EXAMPLES</span></span>

### <span data-ttu-id="ea621-109">範例1：刪除虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="ea621-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="ea621-110">刪除資源群組 "myRG" 中名稱為 "myGateway" 的虛擬網路閘道物件：您必須先使用 **Remove-AzVirtualNetworkGatewayConnection** Cmdlet 刪除虛擬網路閘道的所有連線。</span><span class="sxs-lookup"><span data-stu-id="ea621-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="ea621-111">參數</span><span class="sxs-lookup"><span data-stu-id="ea621-111">PARAMETERS</span></span>

### <span data-ttu-id="ea621-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea621-112">-AsJob</span></span>
<span data-ttu-id="ea621-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ea621-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea621-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea621-114">-DefaultProfile</span></span>
<span data-ttu-id="ea621-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea621-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea621-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ea621-116">-Force</span></span>
<span data-ttu-id="ea621-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ea621-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea621-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea621-118">-Name</span></span>
<span data-ttu-id="ea621-119">指定此 Cmdlet 移除之虛擬網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea621-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea621-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea621-120">-PassThru</span></span>
<span data-ttu-id="ea621-121">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ea621-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ea621-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ea621-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ea621-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea621-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea621-124">指定包含虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea621-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="ea621-125">-確認</span><span class="sxs-lookup"><span data-stu-id="ea621-125">-Confirm</span></span>
<span data-ttu-id="ea621-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea621-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea621-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea621-127">-WhatIf</span></span>
<span data-ttu-id="ea621-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea621-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea621-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea621-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea621-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea621-130">CommonParameters</span></span>
<span data-ttu-id="ea621-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea621-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea621-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ea621-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea621-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ea621-133">INPUTS</span></span>

### <span data-ttu-id="ea621-134">System.object</span><span class="sxs-lookup"><span data-stu-id="ea621-134">System.String</span></span>

## <span data-ttu-id="ea621-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ea621-135">OUTPUTS</span></span>

### <span data-ttu-id="ea621-136">System.object</span><span class="sxs-lookup"><span data-stu-id="ea621-136">System.Boolean</span></span>

## <span data-ttu-id="ea621-137">筆記</span><span class="sxs-lookup"><span data-stu-id="ea621-137">NOTES</span></span>

## <span data-ttu-id="ea621-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea621-138">RELATED LINKS</span></span>

[<span data-ttu-id="ea621-139">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea621-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ea621-140">新-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea621-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ea621-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea621-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ea621-142">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea621-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ea621-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ea621-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
