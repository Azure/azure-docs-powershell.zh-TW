---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 6583856eb6d44fa170b53a855e43db71602534a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446745"
---
# <span data-ttu-id="a6d4e-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a6d4e-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="a6d4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d4e-103">從應用程式閘道取得現有的健康情況探測設定。</span><span class="sxs-lookup"><span data-stu-id="a6d4e-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6d4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6d4e-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6d4e-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6d4e-105">DESCRIPTION</span></span>
<span data-ttu-id="a6d4e-106">Get-AzureRmApplicationGatewayProbeConfig Cmdlet 會從應用程式閘道取得現有的健康情況探測設定。</span><span class="sxs-lookup"><span data-stu-id="a6d4e-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="a6d4e-107">示例</span><span class="sxs-lookup"><span data-stu-id="a6d4e-107">EXAMPLES</span></span>

### <span data-ttu-id="a6d4e-108">範例1：從應用程式閘道取得現有的探測</span><span class="sxs-lookup"><span data-stu-id="a6d4e-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="a6d4e-109">這個命令會從名為「閘道」的應用程式閘道取得名為 Probe02 的 health 探測。</span><span class="sxs-lookup"><span data-stu-id="a6d4e-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="a6d4e-110">參數</span><span class="sxs-lookup"><span data-stu-id="a6d4e-110">PARAMETERS</span></span>

### <span data-ttu-id="a6d4e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6d4e-111">-ApplicationGateway</span></span>
<span data-ttu-id="a6d4e-112">指定此 Cmdlet 取得探測設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="a6d4e-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="a6d4e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6d4e-113">-Name</span></span>
<span data-ttu-id="a6d4e-114">指定探測器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6d4e-114">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="a6d4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d4e-115">-DefaultProfile</span></span>
<span data-ttu-id="a6d4e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6d4e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6d4e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d4e-117">CommonParameters</span></span>
<span data-ttu-id="a6d4e-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6d4e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d4e-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6d4e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d4e-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a6d4e-120">INPUTS</span></span>

### <span data-ttu-id="a6d4e-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a6d4e-121">PSApplicationGateway</span></span>
<span data-ttu-id="a6d4e-122">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a6d4e-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="a6d4e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a6d4e-123">OUTPUTS</span></span>

### <span data-ttu-id="a6d4e-124">PSApplicationGatewayProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a6d4e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="a6d4e-125">[System.object]. IEnumerable "1 [PSApplicationGatewayProbe] （）</span><span class="sxs-lookup"><span data-stu-id="a6d4e-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="a6d4e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a6d4e-126">NOTES</span></span>

## <span data-ttu-id="a6d4e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6d4e-127">RELATED LINKS</span></span>

[<span data-ttu-id="a6d4e-128">新增探測至現有的應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="a6d4e-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="a6d4e-129">附加 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a6d4e-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a6d4e-130">新-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a6d4e-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a6d4e-131">移除-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a6d4e-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="a6d4e-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a6d4e-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

