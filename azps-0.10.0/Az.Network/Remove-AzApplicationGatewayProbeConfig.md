---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 320588b81791c033b94a07261f769fa0886d2f2c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794201"
---
# <span data-ttu-id="fc3c4-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fc3c4-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="fc3c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc3c4-102">SYNOPSIS</span></span>
<span data-ttu-id="fc3c4-103">從現有的應用程式閘道移除健康情況探測。</span><span class="sxs-lookup"><span data-stu-id="fc3c4-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="fc3c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc3c4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc3c4-105">說明</span><span class="sxs-lookup"><span data-stu-id="fc3c4-105">DESCRIPTION</span></span>
<span data-ttu-id="fc3c4-106">Remove-AzApplicationGatewayProbeConfig Cmdlet 會從現有的應用程式閘道移除 heath 探測器。</span><span class="sxs-lookup"><span data-stu-id="fc3c4-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="fc3c4-107">示例</span><span class="sxs-lookup"><span data-stu-id="fc3c4-107">EXAMPLES</span></span>

### <span data-ttu-id="fc3c4-108">範例1：從現有的應用程式閘道移除健康情況探測</span><span class="sxs-lookup"><span data-stu-id="fc3c4-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="fc3c4-109">這個命令會從名為 [閘道] 的應用程式閘道上，移除名為 Probe04 的 health 探測</span><span class="sxs-lookup"><span data-stu-id="fc3c4-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="fc3c4-110">參數</span><span class="sxs-lookup"><span data-stu-id="fc3c4-110">PARAMETERS</span></span>

### <span data-ttu-id="fc3c4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc3c4-111">-ApplicationGateway</span></span>
<span data-ttu-id="fc3c4-112">指定此 Cmdlet 移除探測器的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fc3c4-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="fc3c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc3c4-113">-DefaultProfile</span></span>
<span data-ttu-id="fc3c4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc3c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc3c4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc3c4-115">-Name</span></span>
<span data-ttu-id="fc3c4-116">指定此 Cmdlet 移除的探測器名稱。</span><span class="sxs-lookup"><span data-stu-id="fc3c4-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="fc3c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc3c4-117">CommonParameters</span></span>
<span data-ttu-id="fc3c4-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc3c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc3c4-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc3c4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc3c4-120">輸入</span><span class="sxs-lookup"><span data-stu-id="fc3c4-120">INPUTS</span></span>

### <span data-ttu-id="fc3c4-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fc3c4-121">PSApplicationGateway</span></span>
<span data-ttu-id="fc3c4-122">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="fc3c4-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="fc3c4-123">輸出</span><span class="sxs-lookup"><span data-stu-id="fc3c4-123">OUTPUTS</span></span>

### <span data-ttu-id="fc3c4-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fc3c4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fc3c4-125">筆記</span><span class="sxs-lookup"><span data-stu-id="fc3c4-125">NOTES</span></span>

## <span data-ttu-id="fc3c4-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc3c4-126">RELATED LINKS</span></span>

[<span data-ttu-id="fc3c4-127">從現有的應用程式閘道移除探測器</span><span class="sxs-lookup"><span data-stu-id="fc3c4-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="fc3c4-128">附加 AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fc3c4-128">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fc3c4-129">AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fc3c4-129">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fc3c4-130">新-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fc3c4-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fc3c4-131">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fc3c4-131">Set-AzApplicationGatewayProbeConfig</span></span>]()

