---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 1bdee7a9ffb35085f8194d86dc9a9486f5dd7fb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912793"
---
# <span data-ttu-id="d8973-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d8973-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="d8973-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d8973-102">SYNOPSIS</span></span>
<span data-ttu-id="d8973-103">從應用程式閘道獲得現有的健康狀態檢查組組。</span><span class="sxs-lookup"><span data-stu-id="d8973-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="d8973-104">語法</span><span class="sxs-lookup"><span data-stu-id="d8973-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8973-105">描述</span><span class="sxs-lookup"><span data-stu-id="d8973-105">DESCRIPTION</span></span>
<span data-ttu-id="d8973-106">此Get-AzApplicationGatewayProbeConfig Cmdlet 會從應用程式閘道獲得現有的健康改善組式組式。</span><span class="sxs-lookup"><span data-stu-id="d8973-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="d8973-107">例子</span><span class="sxs-lookup"><span data-stu-id="d8973-107">EXAMPLES</span></span>

### <span data-ttu-id="d8973-108">範例 1：從應用程式閘道取得現有的設計</span><span class="sxs-lookup"><span data-stu-id="d8973-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="d8973-109">此命令會從名為 Gateway 的應用程式閘道中，獲得名為 Command02 的健康狀態指令。</span><span class="sxs-lookup"><span data-stu-id="d8973-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="d8973-110">參數</span><span class="sxs-lookup"><span data-stu-id="d8973-110">PARAMETERS</span></span>

### <span data-ttu-id="d8973-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8973-111">-ApplicationGateway</span></span>
<span data-ttu-id="d8973-112">指定此 Cmdlet 可進行安裝配置的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="d8973-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8973-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8973-113">-DefaultProfile</span></span>
<span data-ttu-id="d8973-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8973-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8973-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8973-115">-Name</span></span>
<span data-ttu-id="d8973-116">指定探索的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8973-116">Specifies the name of the probe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8973-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8973-117">CommonParameters</span></span>
<span data-ttu-id="d8973-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d8973-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8973-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8973-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8973-120">輸入</span><span class="sxs-lookup"><span data-stu-id="d8973-120">INPUTS</span></span>

### <span data-ttu-id="d8973-121">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8973-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8973-122">輸出</span><span class="sxs-lookup"><span data-stu-id="d8973-122">OUTPUTS</span></span>

### <span data-ttu-id="d8973-123">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="d8973-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="d8973-124">筆記</span><span class="sxs-lookup"><span data-stu-id="d8973-124">NOTES</span></span>

## <span data-ttu-id="d8973-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8973-125">RELATED LINKS</span></span>

[<span data-ttu-id="d8973-126">為現有的應用程式閘道新增新結構</span><span class="sxs-lookup"><span data-stu-id="d8973-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="d8973-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d8973-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="d8973-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d8973-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="d8973-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d8973-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="d8973-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d8973-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

