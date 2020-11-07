---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGateway.md
ms.openlocfilehash: 53a4eb40d82a721c93102067c8c7e9fe0cbd86be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795467"
---
# <span data-ttu-id="8b33a-101">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b33a-101">Reset-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="8b33a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b33a-102">SYNOPSIS</span></span>

## <span data-ttu-id="8b33a-103">句法</span><span class="sxs-lookup"><span data-stu-id="8b33a-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> [-GatewayVip <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b33a-104">說明</span><span class="sxs-lookup"><span data-stu-id="8b33a-104">DESCRIPTION</span></span>

## <span data-ttu-id="8b33a-105">示例</span><span class="sxs-lookup"><span data-stu-id="8b33a-105">EXAMPLES</span></span>

### <span data-ttu-id="8b33a-106">sr-1</span><span class="sxs-lookup"><span data-stu-id="8b33a-106">1:</span></span>
```

```

## <span data-ttu-id="8b33a-107">參數</span><span class="sxs-lookup"><span data-stu-id="8b33a-107">PARAMETERS</span></span>

### <span data-ttu-id="8b33a-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b33a-108">-AsJob</span></span>
<span data-ttu-id="8b33a-109">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8b33a-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b33a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b33a-110">-DefaultProfile</span></span>
<span data-ttu-id="8b33a-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b33a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b33a-112">-GatewayVip</span><span class="sxs-lookup"><span data-stu-id="8b33a-112">-GatewayVip</span></span>
<span data-ttu-id="8b33a-113">閘道 vip，以重設特定閘道實例 (例如，在 Active-Active 功能啟用閘道的情況下。 ) 根據預設，如果沒有傳遞任何值，就會重設閘道主要實例。</span><span class="sxs-lookup"><span data-stu-id="8b33a-113">The gateway vip in order to reset particular gateway instance (e.g. in case of Active-Active feature enabled gateways.) By default, gateway primary instance will be reset if no value is passed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b33a-114">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b33a-114">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="8b33a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b33a-115">CommonParameters</span></span>
<span data-ttu-id="8b33a-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b33a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b33a-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b33a-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b33a-118">輸入</span><span class="sxs-lookup"><span data-stu-id="8b33a-118">INPUTS</span></span>

### <span data-ttu-id="8b33a-119">字串</span><span class="sxs-lookup"><span data-stu-id="8b33a-119">String</span></span>
<span data-ttu-id="8b33a-120">"GatewayVip" 參數從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="8b33a-120">Parameter 'GatewayVip' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="8b33a-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b33a-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="8b33a-122">形參 "VirtualNetworkGateway" 接受管線中 "PSVirtualNetworkGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8b33a-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="8b33a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="8b33a-123">OUTPUTS</span></span>

### <span data-ttu-id="8b33a-124">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8b33a-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="8b33a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="8b33a-125">NOTES</span></span>

## <span data-ttu-id="8b33a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b33a-126">RELATED LINKS</span></span>

[<span data-ttu-id="8b33a-127">AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b33a-127">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8b33a-128">新-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b33a-128">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8b33a-129">移除-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b33a-129">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8b33a-130">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b33a-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8b33a-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8b33a-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)


