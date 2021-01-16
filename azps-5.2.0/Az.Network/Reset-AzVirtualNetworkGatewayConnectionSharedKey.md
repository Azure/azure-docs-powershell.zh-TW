---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 496e5aca71d1a947b97c8fd27cab348cee9ba49b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273287"
---
# <span data-ttu-id="20ef1-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="20ef1-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="20ef1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="20ef1-103">重設虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="20ef1-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="20ef1-104">句法</span><span class="sxs-lookup"><span data-stu-id="20ef1-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20ef1-105">說明</span><span class="sxs-lookup"><span data-stu-id="20ef1-105">DESCRIPTION</span></span>
<span data-ttu-id="20ef1-106">重設虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="20ef1-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="20ef1-107">示例</span><span class="sxs-lookup"><span data-stu-id="20ef1-107">EXAMPLES</span></span>

### <span data-ttu-id="20ef1-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="20ef1-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="20ef1-109">參數</span><span class="sxs-lookup"><span data-stu-id="20ef1-109">PARAMETERS</span></span>

### <span data-ttu-id="20ef1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ef1-110">-DefaultProfile</span></span>
<span data-ttu-id="20ef1-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20ef1-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20ef1-112">-Force</span><span class="sxs-lookup"><span data-stu-id="20ef1-112">-Force</span></span>
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

### <span data-ttu-id="20ef1-113">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="20ef1-113">-KeyLength</span></span>
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

### <span data-ttu-id="20ef1-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="20ef1-114">-Name</span></span>
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

### <span data-ttu-id="20ef1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ef1-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="20ef1-116">-確認</span><span class="sxs-lookup"><span data-stu-id="20ef1-116">-Confirm</span></span>
<span data-ttu-id="20ef1-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="20ef1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20ef1-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20ef1-118">-WhatIf</span></span>
<span data-ttu-id="20ef1-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20ef1-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20ef1-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20ef1-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20ef1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ef1-121">CommonParameters</span></span>
<span data-ttu-id="20ef1-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20ef1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ef1-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20ef1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ef1-124">輸入</span><span class="sxs-lookup"><span data-stu-id="20ef1-124">INPUTS</span></span>

### <span data-ttu-id="20ef1-125">System.object</span><span class="sxs-lookup"><span data-stu-id="20ef1-125">System.String</span></span>

### <span data-ttu-id="20ef1-126">UInt32</span><span class="sxs-lookup"><span data-stu-id="20ef1-126">System.UInt32</span></span>

## <span data-ttu-id="20ef1-127">輸出</span><span class="sxs-lookup"><span data-stu-id="20ef1-127">OUTPUTS</span></span>

### <span data-ttu-id="20ef1-128">System.object</span><span class="sxs-lookup"><span data-stu-id="20ef1-128">System.String</span></span>

## <span data-ttu-id="20ef1-129">筆記</span><span class="sxs-lookup"><span data-stu-id="20ef1-129">NOTES</span></span>

## <span data-ttu-id="20ef1-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="20ef1-130">RELATED LINKS</span></span>

[<span data-ttu-id="20ef1-131">AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="20ef1-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="20ef1-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="20ef1-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
