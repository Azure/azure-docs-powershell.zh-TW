---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1c51d58d7732a3f9d07f1beba24a7584b35733b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449597"
---
# <span data-ttu-id="aab4a-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aab4a-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="aab4a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aab4a-102">SYNOPSIS</span></span>
<span data-ttu-id="aab4a-103">配置虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="aab4a-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aab4a-104">句法</span><span class="sxs-lookup"><span data-stu-id="aab4a-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aab4a-105">說明</span><span class="sxs-lookup"><span data-stu-id="aab4a-105">DESCRIPTION</span></span>
<span data-ttu-id="aab4a-106">AzureRmVirtualNetworkGatewayConnectionSharedKey Cmdlet 會 **設定** 虛擬網路閘道連線的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="aab4a-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="aab4a-107">示例</span><span class="sxs-lookup"><span data-stu-id="aab4a-107">EXAMPLES</span></span>

## <span data-ttu-id="aab4a-108">參數</span><span class="sxs-lookup"><span data-stu-id="aab4a-108">PARAMETERS</span></span>

### <span data-ttu-id="aab4a-109">-Force</span><span class="sxs-lookup"><span data-stu-id="aab4a-109">-Force</span></span>
<span data-ttu-id="aab4a-110">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="aab4a-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aab4a-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="aab4a-111">-Name</span></span>
<span data-ttu-id="aab4a-112">指定虛擬網路閘道共用金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="aab4a-112">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="aab4a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aab4a-113">-ResourceGroupName</span></span>
<span data-ttu-id="aab4a-114">指定虛擬網路閘道所屬之資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="aab4a-114">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="aab4a-115">-值</span><span class="sxs-lookup"><span data-stu-id="aab4a-115">-Value</span></span>
<span data-ttu-id="aab4a-116">指定共用金鑰的值。</span><span class="sxs-lookup"><span data-stu-id="aab4a-116">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="aab4a-117">-確認</span><span class="sxs-lookup"><span data-stu-id="aab4a-117">-Confirm</span></span>
<span data-ttu-id="aab4a-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aab4a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aab4a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aab4a-119">-WhatIf</span></span>
<span data-ttu-id="aab4a-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aab4a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aab4a-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aab4a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aab4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab4a-122">-DefaultProfile</span></span>
<span data-ttu-id="aab4a-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aab4a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aab4a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab4a-124">CommonParameters</span></span>
<span data-ttu-id="aab4a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aab4a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab4a-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aab4a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab4a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="aab4a-127">INPUTS</span></span>

## <span data-ttu-id="aab4a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="aab4a-128">OUTPUTS</span></span>

### <span data-ttu-id="aab4a-129">System.object</span><span class="sxs-lookup"><span data-stu-id="aab4a-129">System.String</span></span>

## <span data-ttu-id="aab4a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="aab4a-130">NOTES</span></span>

## <span data-ttu-id="aab4a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="aab4a-131">RELATED LINKS</span></span>

[<span data-ttu-id="aab4a-132">AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aab4a-132">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="aab4a-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="aab4a-133">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


