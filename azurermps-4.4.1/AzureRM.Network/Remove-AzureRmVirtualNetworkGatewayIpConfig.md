---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: d721feb80598e343fc5757eceee90136bbc51ae9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457252"
---
# <span data-ttu-id="bac92-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="bac92-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="bac92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bac92-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bac92-103">句法</span><span class="sxs-lookup"><span data-stu-id="bac92-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bac92-104">說明</span><span class="sxs-lookup"><span data-stu-id="bac92-104">DESCRIPTION</span></span>

## <span data-ttu-id="bac92-105">示例</span><span class="sxs-lookup"><span data-stu-id="bac92-105">EXAMPLES</span></span>

### <span data-ttu-id="bac92-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="bac92-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="bac92-107">參數</span><span class="sxs-lookup"><span data-stu-id="bac92-107">PARAMETERS</span></span>

### <span data-ttu-id="bac92-108">-名稱</span><span class="sxs-lookup"><span data-stu-id="bac92-108">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bac92-109">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bac92-109">-VirtualNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bac92-110">-確認</span><span class="sxs-lookup"><span data-stu-id="bac92-110">-Confirm</span></span>
<span data-ttu-id="bac92-111">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bac92-111">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bac92-112">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bac92-112">-WhatIf</span></span>
<span data-ttu-id="bac92-113">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bac92-113">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bac92-114">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bac92-114">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bac92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac92-115">-DefaultProfile</span></span>
<span data-ttu-id="bac92-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bac92-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bac92-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac92-117">CommonParameters</span></span>
<span data-ttu-id="bac92-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bac92-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac92-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bac92-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac92-120">輸入</span><span class="sxs-lookup"><span data-stu-id="bac92-120">INPUTS</span></span>

### <span data-ttu-id="bac92-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bac92-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="bac92-122">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="bac92-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="bac92-123">輸出</span><span class="sxs-lookup"><span data-stu-id="bac92-123">OUTPUTS</span></span>

### <span data-ttu-id="bac92-124">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bac92-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="bac92-125">筆記</span><span class="sxs-lookup"><span data-stu-id="bac92-125">NOTES</span></span>

## <span data-ttu-id="bac92-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="bac92-126">RELATED LINKS</span></span>

