---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a805145445f8bd17ac60497e2c7d7e89ea56a3c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456171"
---
# <span data-ttu-id="9e24d-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="9e24d-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="9e24d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e24d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e24d-103">句法</span><span class="sxs-lookup"><span data-stu-id="9e24d-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e24d-104">說明</span><span class="sxs-lookup"><span data-stu-id="9e24d-104">DESCRIPTION</span></span>

## <span data-ttu-id="9e24d-105">示例</span><span class="sxs-lookup"><span data-stu-id="9e24d-105">EXAMPLES</span></span>

## <span data-ttu-id="9e24d-106">參數</span><span class="sxs-lookup"><span data-stu-id="9e24d-106">PARAMETERS</span></span>

### <span data-ttu-id="9e24d-107">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e24d-107">-DefaultProfile</span></span>
<span data-ttu-id="9e24d-108">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e24d-108">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e24d-109">-Force</span><span class="sxs-lookup"><span data-stu-id="9e24d-109">-Force</span></span>
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

### <span data-ttu-id="9e24d-110">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="9e24d-110">-KeyLength</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e24d-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e24d-111">-Name</span></span>
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

### <span data-ttu-id="9e24d-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e24d-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="9e24d-113">-確認</span><span class="sxs-lookup"><span data-stu-id="9e24d-113">-Confirm</span></span>
<span data-ttu-id="9e24d-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e24d-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e24d-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e24d-115">-WhatIf</span></span>
<span data-ttu-id="9e24d-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e24d-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e24d-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e24d-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e24d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e24d-118">CommonParameters</span></span>
<span data-ttu-id="9e24d-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e24d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e24d-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e24d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e24d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="9e24d-121">INPUTS</span></span>

### <span data-ttu-id="9e24d-122">所有</span><span class="sxs-lookup"><span data-stu-id="9e24d-122">None</span></span>
<span data-ttu-id="9e24d-123">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9e24d-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e24d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9e24d-124">OUTPUTS</span></span>

### <span data-ttu-id="9e24d-125">System.object</span><span class="sxs-lookup"><span data-stu-id="9e24d-125">System.String</span></span>

## <span data-ttu-id="9e24d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9e24d-126">NOTES</span></span>

## <span data-ttu-id="9e24d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e24d-127">RELATED LINKS</span></span>

[<span data-ttu-id="9e24d-128">AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="9e24d-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="9e24d-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="9e24d-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


