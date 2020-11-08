---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128447"
---
# <span data-ttu-id="457f5-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="457f5-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="457f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="457f5-102">SYNOPSIS</span></span>
<span data-ttu-id="457f5-103">從應用程式閘道取得現有的健康情況探測設定。</span><span class="sxs-lookup"><span data-stu-id="457f5-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="457f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="457f5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="457f5-105">說明</span><span class="sxs-lookup"><span data-stu-id="457f5-105">DESCRIPTION</span></span>
<span data-ttu-id="457f5-106">Get-AzApplicationGatewayProbeConfig Cmdlet 會從應用程式閘道取得現有的健康情況探測設定。</span><span class="sxs-lookup"><span data-stu-id="457f5-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="457f5-107">示例</span><span class="sxs-lookup"><span data-stu-id="457f5-107">EXAMPLES</span></span>

### <span data-ttu-id="457f5-108">範例1：從應用程式閘道取得現有的探測</span><span class="sxs-lookup"><span data-stu-id="457f5-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="457f5-109">這個命令會從名為「閘道」的應用程式閘道取得名為 Probe02 的 health 探測。</span><span class="sxs-lookup"><span data-stu-id="457f5-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="457f5-110">參數</span><span class="sxs-lookup"><span data-stu-id="457f5-110">PARAMETERS</span></span>

### <span data-ttu-id="457f5-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="457f5-111">-ApplicationGateway</span></span>
<span data-ttu-id="457f5-112">指定此 Cmdlet 取得探測設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="457f5-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="457f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="457f5-113">-DefaultProfile</span></span>
<span data-ttu-id="457f5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="457f5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="457f5-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="457f5-115">-Name</span></span>
<span data-ttu-id="457f5-116">指定探測器的名稱。</span><span class="sxs-lookup"><span data-stu-id="457f5-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="457f5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="457f5-117">CommonParameters</span></span>
<span data-ttu-id="457f5-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="457f5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="457f5-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="457f5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="457f5-120">輸入</span><span class="sxs-lookup"><span data-stu-id="457f5-120">INPUTS</span></span>

### <span data-ttu-id="457f5-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="457f5-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="457f5-122">輸出</span><span class="sxs-lookup"><span data-stu-id="457f5-122">OUTPUTS</span></span>

### <span data-ttu-id="457f5-123">PSApplicationGatewayProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="457f5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="457f5-124">筆記</span><span class="sxs-lookup"><span data-stu-id="457f5-124">NOTES</span></span>

## <span data-ttu-id="457f5-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="457f5-125">RELATED LINKS</span></span>

[<span data-ttu-id="457f5-126">新增探測至現有的應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="457f5-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="457f5-127">附加 AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="457f5-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="457f5-128">新-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="457f5-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="457f5-129">移除-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="457f5-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="457f5-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="457f5-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

