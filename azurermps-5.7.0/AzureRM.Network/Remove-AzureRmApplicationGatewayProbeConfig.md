---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 14d1aea928923d9da4eee089ae1e95c75289eb3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626149"
---
# <span data-ttu-id="58b0b-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="58b0b-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="58b0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="58b0b-103">從現有的應用程式閘道移除健康情況探測。</span><span class="sxs-lookup"><span data-stu-id="58b0b-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58b0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="58b0b-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58b0b-105">說明</span><span class="sxs-lookup"><span data-stu-id="58b0b-105">DESCRIPTION</span></span>
<span data-ttu-id="58b0b-106">Remove-AzureRmApplicationGatewayProbeConfig Cmdlet 會從現有的應用程式閘道移除 heath 探測器。</span><span class="sxs-lookup"><span data-stu-id="58b0b-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="58b0b-107">示例</span><span class="sxs-lookup"><span data-stu-id="58b0b-107">EXAMPLES</span></span>

### <span data-ttu-id="58b0b-108">範例1：從現有的應用程式閘道移除健康情況探測</span><span class="sxs-lookup"><span data-stu-id="58b0b-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="58b0b-109">這個命令會從名為 [閘道] 的應用程式閘道上，移除名為 Probe04 的 health 探測</span><span class="sxs-lookup"><span data-stu-id="58b0b-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="58b0b-110">參數</span><span class="sxs-lookup"><span data-stu-id="58b0b-110">PARAMETERS</span></span>

### <span data-ttu-id="58b0b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58b0b-111">-ApplicationGateway</span></span>
<span data-ttu-id="58b0b-112">指定此 Cmdlet 移除探測器的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="58b0b-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="58b0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b0b-113">-DefaultProfile</span></span>
<span data-ttu-id="58b0b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58b0b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58b0b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="58b0b-115">-Name</span></span>
<span data-ttu-id="58b0b-116">指定此 Cmdlet 移除的探測器名稱。</span><span class="sxs-lookup"><span data-stu-id="58b0b-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="58b0b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b0b-117">CommonParameters</span></span>
<span data-ttu-id="58b0b-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58b0b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b0b-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58b0b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b0b-120">輸入</span><span class="sxs-lookup"><span data-stu-id="58b0b-120">INPUTS</span></span>

### <span data-ttu-id="58b0b-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58b0b-121">PSApplicationGateway</span></span>
<span data-ttu-id="58b0b-122">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="58b0b-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="58b0b-123">輸出</span><span class="sxs-lookup"><span data-stu-id="58b0b-123">OUTPUTS</span></span>

### <span data-ttu-id="58b0b-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="58b0b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="58b0b-125">筆記</span><span class="sxs-lookup"><span data-stu-id="58b0b-125">NOTES</span></span>

## <span data-ttu-id="58b0b-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="58b0b-126">RELATED LINKS</span></span>

[<span data-ttu-id="58b0b-127">從現有的應用程式閘道移除探測器</span><span class="sxs-lookup"><span data-stu-id="58b0b-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="58b0b-128">附加 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="58b0b-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="58b0b-129">AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="58b0b-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="58b0b-130">新-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="58b0b-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="58b0b-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="58b0b-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

