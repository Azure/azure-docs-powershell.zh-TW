---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 6b2121c581d3d7da990813884cf0097064b73f44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908809"
---
# <span data-ttu-id="86212-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="86212-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="86212-102">簡介</span><span class="sxs-lookup"><span data-stu-id="86212-102">SYNOPSIS</span></span>
<span data-ttu-id="86212-103">重設虛擬網路閘道連接的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="86212-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="86212-104">語法</span><span class="sxs-lookup"><span data-stu-id="86212-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86212-105">描述</span><span class="sxs-lookup"><span data-stu-id="86212-105">DESCRIPTION</span></span>
<span data-ttu-id="86212-106">重設虛擬網路閘道連接的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="86212-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="86212-107">例子</span><span class="sxs-lookup"><span data-stu-id="86212-107">EXAMPLES</span></span>

### <span data-ttu-id="86212-108">範例 1：</span><span class="sxs-lookup"><span data-stu-id="86212-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="86212-109">參數</span><span class="sxs-lookup"><span data-stu-id="86212-109">PARAMETERS</span></span>

### <span data-ttu-id="86212-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86212-110">-DefaultProfile</span></span>
<span data-ttu-id="86212-111">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="86212-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86212-112">-強制</span><span class="sxs-lookup"><span data-stu-id="86212-112">-Force</span></span>
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

### <span data-ttu-id="86212-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="86212-113">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86212-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="86212-114">-Name</span></span>
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

### <span data-ttu-id="86212-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86212-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="86212-116">-確認</span><span class="sxs-lookup"><span data-stu-id="86212-116">-Confirm</span></span>
<span data-ttu-id="86212-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="86212-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86212-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86212-118">-WhatIf</span></span>
<span data-ttu-id="86212-119">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="86212-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86212-120">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="86212-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86212-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86212-121">CommonParameters</span></span>
<span data-ttu-id="86212-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="86212-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86212-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="86212-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86212-124">輸入</span><span class="sxs-lookup"><span data-stu-id="86212-124">INPUTS</span></span>

### <span data-ttu-id="86212-125">System.String</span><span class="sxs-lookup"><span data-stu-id="86212-125">System.String</span></span>

### <span data-ttu-id="86212-126">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="86212-126">System.UInt32</span></span>

## <span data-ttu-id="86212-127">輸出</span><span class="sxs-lookup"><span data-stu-id="86212-127">OUTPUTS</span></span>

### <span data-ttu-id="86212-128">System.String</span><span class="sxs-lookup"><span data-stu-id="86212-128">System.String</span></span>

## <span data-ttu-id="86212-129">筆記</span><span class="sxs-lookup"><span data-stu-id="86212-129">NOTES</span></span>

## <span data-ttu-id="86212-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="86212-130">RELATED LINKS</span></span>

[<span data-ttu-id="86212-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="86212-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="86212-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="86212-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
