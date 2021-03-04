---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3a598001421bf237f93a63fb4f45d069bf9404ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915957"
---
# <span data-ttu-id="7a06a-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7a06a-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="7a06a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7a06a-102">SYNOPSIS</span></span>
<span data-ttu-id="7a06a-103">刪除虛擬網路閘道連接</span><span class="sxs-lookup"><span data-stu-id="7a06a-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="7a06a-104">語法</span><span class="sxs-lookup"><span data-stu-id="7a06a-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a06a-105">描述</span><span class="sxs-lookup"><span data-stu-id="7a06a-105">DESCRIPTION</span></span>
<span data-ttu-id="7a06a-106">虛擬網路閘道連接是代表 IPsec 服務物件 (網站對網站或 Vnet-to-Vnet) 連接至 Azure 中的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="7a06a-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7a06a-107">**Remove-AzVirtualNetworkGatewayConnection** Cmdlet 會根據您的名稱和資源組名刪除您的連線物件。</span><span class="sxs-lookup"><span data-stu-id="7a06a-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="7a06a-108">例子</span><span class="sxs-lookup"><span data-stu-id="7a06a-108">EXAMPLES</span></span>

### <span data-ttu-id="7a06a-109">範例 1：刪除虛擬網路閘道連接</span><span class="sxs-lookup"><span data-stu-id="7a06a-109">Example 1: Delete a Virtual Network Gateway Connection</span></span>
```powershell
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="7a06a-110">刪除資源群組 "myRG" 中名稱為 "myTun圳" 的虛擬網路閘道連線物件</span><span class="sxs-lookup"><span data-stu-id="7a06a-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="7a06a-111">參數</span><span class="sxs-lookup"><span data-stu-id="7a06a-111">PARAMETERS</span></span>

### <span data-ttu-id="7a06a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a06a-112">-DefaultProfile</span></span>
<span data-ttu-id="7a06a-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a06a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a06a-114">-強制</span><span class="sxs-lookup"><span data-stu-id="7a06a-114">-Force</span></span>
<span data-ttu-id="7a06a-115">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7a06a-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a06a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a06a-116">-Name</span></span>
<span data-ttu-id="7a06a-117">指定此 Cmdlet 移除的虛擬網路閘道連接名稱。</span><span class="sxs-lookup"><span data-stu-id="7a06a-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a06a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a06a-118">-PassThru</span></span>
<span data-ttu-id="7a06a-119">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="7a06a-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7a06a-120">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7a06a-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7a06a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a06a-121">-ResourceGroupName</span></span>
<span data-ttu-id="7a06a-122">指定包含虛擬網路閘道連接的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7a06a-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="7a06a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="7a06a-123">-Confirm</span></span>
<span data-ttu-id="7a06a-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7a06a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a06a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a06a-125">-WhatIf</span></span>
<span data-ttu-id="7a06a-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7a06a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a06a-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a06a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a06a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a06a-128">CommonParameters</span></span>
<span data-ttu-id="7a06a-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7a06a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a06a-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7a06a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a06a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7a06a-131">INPUTS</span></span>

### <span data-ttu-id="7a06a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7a06a-132">System.String</span></span>

## <span data-ttu-id="7a06a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7a06a-133">OUTPUTS</span></span>

### <span data-ttu-id="7a06a-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a06a-134">System.Boolean</span></span>

## <span data-ttu-id="7a06a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7a06a-135">NOTES</span></span>

## <span data-ttu-id="7a06a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a06a-136">RELATED LINKS</span></span>

[<span data-ttu-id="7a06a-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7a06a-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7a06a-138">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7a06a-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="7a06a-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="7a06a-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
