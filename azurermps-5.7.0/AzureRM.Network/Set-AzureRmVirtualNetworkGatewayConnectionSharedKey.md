---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 2f6af6dbbe8a7241cb25e1715859a68bec24598c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447750"
---
# <span data-ttu-id="ce2c7-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ce2c7-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="ce2c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ce2c7-103">配置虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce2c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce2c7-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce2c7-105">說明</span><span class="sxs-lookup"><span data-stu-id="ce2c7-105">DESCRIPTION</span></span>
<span data-ttu-id="ce2c7-106">AzureRmVirtualNetworkGatewayConnectionSharedKey Cmdlet 會 **設定** 虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="ce2c7-107">示例</span><span class="sxs-lookup"><span data-stu-id="ce2c7-107">EXAMPLES</span></span>

## <span data-ttu-id="ce2c7-108">參數</span><span class="sxs-lookup"><span data-stu-id="ce2c7-108">PARAMETERS</span></span>

### <span data-ttu-id="ce2c7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce2c7-109">-DefaultProfile</span></span>
<span data-ttu-id="ce2c7-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce2c7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ce2c7-111">-Force</span></span>
<span data-ttu-id="ce2c7-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce2c7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce2c7-113">-Name</span></span>
<span data-ttu-id="ce2c7-114">指定虛擬網路閘道共用金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-114">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="ce2c7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce2c7-115">-ResourceGroupName</span></span>
<span data-ttu-id="ce2c7-116">指定虛擬網路閘道所屬之資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="ce2c7-116">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="ce2c7-117">-值</span><span class="sxs-lookup"><span data-stu-id="ce2c7-117">-Value</span></span>
<span data-ttu-id="ce2c7-118">指定共用金鑰的值。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-118">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="ce2c7-119">-確認</span><span class="sxs-lookup"><span data-stu-id="ce2c7-119">-Confirm</span></span>
<span data-ttu-id="ce2c7-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce2c7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce2c7-121">-WhatIf</span></span>
<span data-ttu-id="ce2c7-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce2c7-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce2c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce2c7-124">CommonParameters</span></span>
<span data-ttu-id="ce2c7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce2c7-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce2c7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ce2c7-127">INPUTS</span></span>

### <span data-ttu-id="ce2c7-128">所有</span><span class="sxs-lookup"><span data-stu-id="ce2c7-128">None</span></span>
<span data-ttu-id="ce2c7-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ce2c7-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce2c7-130">輸出</span><span class="sxs-lookup"><span data-stu-id="ce2c7-130">OUTPUTS</span></span>

### <span data-ttu-id="ce2c7-131">System.object</span><span class="sxs-lookup"><span data-stu-id="ce2c7-131">System.String</span></span>

## <span data-ttu-id="ce2c7-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ce2c7-132">NOTES</span></span>

## <span data-ttu-id="ce2c7-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce2c7-133">RELATED LINKS</span></span>

[<span data-ttu-id="ce2c7-134">AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ce2c7-134">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="ce2c7-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ce2c7-135">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


