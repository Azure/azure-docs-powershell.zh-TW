---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 6be6c0d7993b44d807cad5bf8c06a203fe8ff7a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625611"
---
# <span data-ttu-id="e3f00-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="e3f00-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="e3f00-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3f00-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3f00-103">句法</span><span class="sxs-lookup"><span data-stu-id="e3f00-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3f00-104">說明</span><span class="sxs-lookup"><span data-stu-id="e3f00-104">DESCRIPTION</span></span>

## <span data-ttu-id="e3f00-105">示例</span><span class="sxs-lookup"><span data-stu-id="e3f00-105">EXAMPLES</span></span>

### <span data-ttu-id="e3f00-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="e3f00-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e3f00-107">參數</span><span class="sxs-lookup"><span data-stu-id="e3f00-107">PARAMETERS</span></span>

### <span data-ttu-id="e3f00-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f00-108">-DefaultProfile</span></span>
<span data-ttu-id="e3f00-109">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3f00-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3f00-110">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3f00-110">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3f00-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3f00-111">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3f00-112">-確認</span><span class="sxs-lookup"><span data-stu-id="e3f00-112">-Confirm</span></span>
<span data-ttu-id="e3f00-113">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3f00-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3f00-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3f00-114">-WhatIf</span></span>
<span data-ttu-id="e3f00-115">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3f00-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3f00-116">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3f00-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3f00-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f00-117">CommonParameters</span></span>
<span data-ttu-id="e3f00-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3f00-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f00-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3f00-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f00-120">輸入</span><span class="sxs-lookup"><span data-stu-id="e3f00-120">INPUTS</span></span>

### <span data-ttu-id="e3f00-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e3f00-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="e3f00-122">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="e3f00-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="e3f00-123">輸出</span><span class="sxs-lookup"><span data-stu-id="e3f00-123">OUTPUTS</span></span>

### <span data-ttu-id="e3f00-124">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3f00-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="e3f00-125">筆記</span><span class="sxs-lookup"><span data-stu-id="e3f00-125">NOTES</span></span>

## <span data-ttu-id="e3f00-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3f00-126">RELATED LINKS</span></span>

