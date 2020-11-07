---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: f68709cad84adb6904e509472b1c960d6134144c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800353"
---
# <span data-ttu-id="799ee-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="799ee-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="799ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="799ee-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="799ee-103">句法</span><span class="sxs-lookup"><span data-stu-id="799ee-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="799ee-104">說明</span><span class="sxs-lookup"><span data-stu-id="799ee-104">DESCRIPTION</span></span>

## <span data-ttu-id="799ee-105">示例</span><span class="sxs-lookup"><span data-stu-id="799ee-105">EXAMPLES</span></span>

### <span data-ttu-id="799ee-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="799ee-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="799ee-107">參數</span><span class="sxs-lookup"><span data-stu-id="799ee-107">PARAMETERS</span></span>

### <span data-ttu-id="799ee-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="799ee-108">-DefaultProfile</span></span>
<span data-ttu-id="799ee-109">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="799ee-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="799ee-110">-名稱</span><span class="sxs-lookup"><span data-stu-id="799ee-110">-Name</span></span>
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

### <span data-ttu-id="799ee-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="799ee-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="799ee-112">-確認</span><span class="sxs-lookup"><span data-stu-id="799ee-112">-Confirm</span></span>
<span data-ttu-id="799ee-113">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="799ee-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="799ee-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="799ee-114">-WhatIf</span></span>
<span data-ttu-id="799ee-115">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="799ee-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="799ee-116">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="799ee-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="799ee-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="799ee-117">CommonParameters</span></span>
<span data-ttu-id="799ee-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="799ee-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="799ee-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="799ee-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="799ee-120">輸入</span><span class="sxs-lookup"><span data-stu-id="799ee-120">INPUTS</span></span>

### <span data-ttu-id="799ee-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="799ee-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="799ee-122">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="799ee-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="799ee-123">輸出</span><span class="sxs-lookup"><span data-stu-id="799ee-123">OUTPUTS</span></span>

### <span data-ttu-id="799ee-124">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="799ee-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="799ee-125">筆記</span><span class="sxs-lookup"><span data-stu-id="799ee-125">NOTES</span></span>

## <span data-ttu-id="799ee-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="799ee-126">RELATED LINKS</span></span>

