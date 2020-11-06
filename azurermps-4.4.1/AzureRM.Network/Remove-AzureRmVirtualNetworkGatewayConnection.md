---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d2068273c6f46c058ad7586083f6bfa0db037cab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448128"
---
# <span data-ttu-id="715d0-101">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="715d0-101">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="715d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="715d0-102">SYNOPSIS</span></span>
<span data-ttu-id="715d0-103">刪除虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="715d0-103">Deletes a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="715d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="715d0-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="715d0-105">說明</span><span class="sxs-lookup"><span data-stu-id="715d0-105">DESCRIPTION</span></span>
<span data-ttu-id="715d0-106">虛擬網路閘道連線是代表連接至 Azure 中虛擬網路閘道的 IPsec 隧道 (點對點或 Vnet 到 Vnet) 的物件。</span><span class="sxs-lookup"><span data-stu-id="715d0-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="715d0-107">**AzureRmVirtualNetworkGatewayConnection** Cmdlet 會根據名稱和資源組名稱來刪除連線物件。</span><span class="sxs-lookup"><span data-stu-id="715d0-107">The **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="715d0-108">示例</span><span class="sxs-lookup"><span data-stu-id="715d0-108">EXAMPLES</span></span>

### <span data-ttu-id="715d0-109">1：刪除虛擬網路閘道連線</span><span class="sxs-lookup"><span data-stu-id="715d0-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="715d0-110">刪除資源群組 "myRG" 中名稱為 "myTunnel" 的虛擬網路閘道連線物件</span><span class="sxs-lookup"><span data-stu-id="715d0-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="715d0-111">參數</span><span class="sxs-lookup"><span data-stu-id="715d0-111">PARAMETERS</span></span>

### <span data-ttu-id="715d0-112">-Force</span><span class="sxs-lookup"><span data-stu-id="715d0-112">-Force</span></span>
<span data-ttu-id="715d0-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="715d0-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="715d0-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="715d0-114">-Name</span></span>
<span data-ttu-id="715d0-115">指定此 Cmdlet 移除的虛擬網路閘道連線名稱。</span><span class="sxs-lookup"><span data-stu-id="715d0-115">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="715d0-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="715d0-116">-PassThru</span></span>
<span data-ttu-id="715d0-117">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="715d0-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="715d0-118">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="715d0-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="715d0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="715d0-119">-ResourceGroupName</span></span>
<span data-ttu-id="715d0-120">指定包含虛擬網路閘道連線之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="715d0-120">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="715d0-121">-確認</span><span class="sxs-lookup"><span data-stu-id="715d0-121">-Confirm</span></span>
<span data-ttu-id="715d0-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="715d0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="715d0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="715d0-123">-WhatIf</span></span>
<span data-ttu-id="715d0-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="715d0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="715d0-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="715d0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="715d0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715d0-126">-DefaultProfile</span></span>
<span data-ttu-id="715d0-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="715d0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="715d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715d0-128">CommonParameters</span></span>
<span data-ttu-id="715d0-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="715d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715d0-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="715d0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715d0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="715d0-131">INPUTS</span></span>

## <span data-ttu-id="715d0-132">輸出</span><span class="sxs-lookup"><span data-stu-id="715d0-132">OUTPUTS</span></span>

## <span data-ttu-id="715d0-133">筆記</span><span class="sxs-lookup"><span data-stu-id="715d0-133">NOTES</span></span>

## <span data-ttu-id="715d0-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="715d0-134">RELATED LINKS</span></span>

[<span data-ttu-id="715d0-135">AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="715d0-135">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="715d0-136">新-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="715d0-136">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="715d0-137">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="715d0-137">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)


