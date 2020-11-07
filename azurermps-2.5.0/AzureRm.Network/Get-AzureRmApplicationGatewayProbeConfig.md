---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: cbe38933cb4c2c75b5219bf0deccc0b28052a61f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800869"
---
# <span data-ttu-id="20f47-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="20f47-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="20f47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20f47-102">SYNOPSIS</span></span>
<span data-ttu-id="20f47-103">從應用程式閘道取得現有的健康情況探測設定。</span><span class="sxs-lookup"><span data-stu-id="20f47-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20f47-104">句法</span><span class="sxs-lookup"><span data-stu-id="20f47-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20f47-105">說明</span><span class="sxs-lookup"><span data-stu-id="20f47-105">DESCRIPTION</span></span>
<span data-ttu-id="20f47-106">Get-AzureRmApplicationGatewayProbeConfig Cmdlet 會從應用程式閘道取得現有的健康情況探測設定。</span><span class="sxs-lookup"><span data-stu-id="20f47-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="20f47-107">示例</span><span class="sxs-lookup"><span data-stu-id="20f47-107">EXAMPLES</span></span>

### <span data-ttu-id="20f47-108">範例1：從應用程式閘道取得現有的探測</span><span class="sxs-lookup"><span data-stu-id="20f47-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="20f47-109">這個命令會從名為「閘道」的應用程式閘道取得名為 Probe02 的 health 探測。</span><span class="sxs-lookup"><span data-stu-id="20f47-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="20f47-110">參數</span><span class="sxs-lookup"><span data-stu-id="20f47-110">PARAMETERS</span></span>

### <span data-ttu-id="20f47-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20f47-111">-ApplicationGateway</span></span>
<span data-ttu-id="20f47-112">指定此 Cmdlet 取得探測設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="20f47-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="20f47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f47-113">-DefaultProfile</span></span>
<span data-ttu-id="20f47-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20f47-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20f47-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="20f47-115">-Name</span></span>
<span data-ttu-id="20f47-116">指定探測器的名稱。</span><span class="sxs-lookup"><span data-stu-id="20f47-116">Specifies the name of the probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20f47-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f47-117">CommonParameters</span></span>
<span data-ttu-id="20f47-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20f47-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f47-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="20f47-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f47-120">輸入</span><span class="sxs-lookup"><span data-stu-id="20f47-120">INPUTS</span></span>

### <span data-ttu-id="20f47-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20f47-121">PSApplicationGateway</span></span>
<span data-ttu-id="20f47-122">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="20f47-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="20f47-123">輸出</span><span class="sxs-lookup"><span data-stu-id="20f47-123">OUTPUTS</span></span>

### <span data-ttu-id="20f47-124">PSApplicationGatewayProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="20f47-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="20f47-125">[System.object]. IEnumerable "1 [PSApplicationGatewayProbe] （）</span><span class="sxs-lookup"><span data-stu-id="20f47-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="20f47-126">筆記</span><span class="sxs-lookup"><span data-stu-id="20f47-126">NOTES</span></span>

## <span data-ttu-id="20f47-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="20f47-127">RELATED LINKS</span></span>

[<span data-ttu-id="20f47-128">新增探測至現有的應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="20f47-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="20f47-129">附加 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="20f47-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="20f47-130">新-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="20f47-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="20f47-131">移除-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="20f47-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="20f47-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="20f47-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

