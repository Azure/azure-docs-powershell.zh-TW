---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 39ce61f4a1e973dfdac8104a6364bdd3d8b9151a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802009"
---
# <span data-ttu-id="4b99c-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4b99c-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="4b99c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b99c-102">SYNOPSIS</span></span>
<span data-ttu-id="4b99c-103">從現有的應用程式閘道移除健康情況探測。</span><span class="sxs-lookup"><span data-stu-id="4b99c-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b99c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b99c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b99c-105">說明</span><span class="sxs-lookup"><span data-stu-id="4b99c-105">DESCRIPTION</span></span>
<span data-ttu-id="4b99c-106">Remove-AzureRmApplicationGatewayProbeConfig Cmdlet 會從現有的應用程式閘道移除 heath 探測器。</span><span class="sxs-lookup"><span data-stu-id="4b99c-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="4b99c-107">示例</span><span class="sxs-lookup"><span data-stu-id="4b99c-107">EXAMPLES</span></span>

### <span data-ttu-id="4b99c-108">範例1：從現有的應用程式閘道移除健康情況探測</span><span class="sxs-lookup"><span data-stu-id="4b99c-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="4b99c-109">這個命令會從名為 [閘道] 的應用程式閘道上，移除名為 Probe04 的 health 探測</span><span class="sxs-lookup"><span data-stu-id="4b99c-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="4b99c-110">參數</span><span class="sxs-lookup"><span data-stu-id="4b99c-110">PARAMETERS</span></span>

### <span data-ttu-id="4b99c-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b99c-111">-ApplicationGateway</span></span>
<span data-ttu-id="4b99c-112">指定此 Cmdlet 移除探測器的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4b99c-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b99c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b99c-113">-DefaultProfile</span></span>
<span data-ttu-id="4b99c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b99c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b99c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b99c-115">-Name</span></span>
<span data-ttu-id="4b99c-116">指定此 Cmdlet 移除的探測器名稱。</span><span class="sxs-lookup"><span data-stu-id="4b99c-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="4b99c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b99c-117">CommonParameters</span></span>
<span data-ttu-id="4b99c-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b99c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b99c-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b99c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b99c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4b99c-120">INPUTS</span></span>

### <span data-ttu-id="4b99c-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b99c-121">PSApplicationGateway</span></span>
<span data-ttu-id="4b99c-122">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="4b99c-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="4b99c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="4b99c-123">OUTPUTS</span></span>

### <span data-ttu-id="4b99c-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4b99c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4b99c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="4b99c-125">NOTES</span></span>

## <span data-ttu-id="4b99c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b99c-126">RELATED LINKS</span></span>

[<span data-ttu-id="4b99c-127">從現有的應用程式閘道移除探測器</span><span class="sxs-lookup"><span data-stu-id="4b99c-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="4b99c-128">附加 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4b99c-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4b99c-129">AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4b99c-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4b99c-130">新-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4b99c-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4b99c-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4b99c-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

