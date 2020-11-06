---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 2730e3ba1e85a876940492b4abfd4fbe5dbca956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452803"
---
# <span data-ttu-id="7c939-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7c939-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="7c939-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c939-102">SYNOPSIS</span></span>
<span data-ttu-id="7c939-103">從應用程式閘道取得現有的健康情況探測設定。</span><span class="sxs-lookup"><span data-stu-id="7c939-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c939-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c939-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c939-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c939-105">DESCRIPTION</span></span>
<span data-ttu-id="7c939-106">Get-AzureRmApplicationGatewayProbeConfig Cmdlet 會從應用程式閘道取得現有的健康情況探測設定。</span><span class="sxs-lookup"><span data-stu-id="7c939-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="7c939-107">示例</span><span class="sxs-lookup"><span data-stu-id="7c939-107">EXAMPLES</span></span>

### <span data-ttu-id="7c939-108">範例1：從應用程式閘道取得現有的探測</span><span class="sxs-lookup"><span data-stu-id="7c939-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="7c939-109">這個命令會從名為「閘道」的應用程式閘道取得名為 Probe02 的 health 探測。</span><span class="sxs-lookup"><span data-stu-id="7c939-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="7c939-110">參數</span><span class="sxs-lookup"><span data-stu-id="7c939-110">PARAMETERS</span></span>

### <span data-ttu-id="7c939-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c939-111">-ApplicationGateway</span></span>
<span data-ttu-id="7c939-112">指定此 Cmdlet 取得探測設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="7c939-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="7c939-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c939-113">-DefaultProfile</span></span>
<span data-ttu-id="7c939-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c939-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c939-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c939-115">-Name</span></span>
<span data-ttu-id="7c939-116">指定探測器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c939-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="7c939-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c939-117">CommonParameters</span></span>
<span data-ttu-id="7c939-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c939-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c939-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c939-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c939-120">輸入</span><span class="sxs-lookup"><span data-stu-id="7c939-120">INPUTS</span></span>

### <span data-ttu-id="7c939-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7c939-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="7c939-122">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="7c939-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="7c939-123">輸出</span><span class="sxs-lookup"><span data-stu-id="7c939-123">OUTPUTS</span></span>

### <span data-ttu-id="7c939-124">PSApplicationGatewayProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7c939-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="7c939-125">筆記</span><span class="sxs-lookup"><span data-stu-id="7c939-125">NOTES</span></span>

## <span data-ttu-id="7c939-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c939-126">RELATED LINKS</span></span>

[<span data-ttu-id="7c939-127">新增探測至現有的應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="7c939-127">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="7c939-128">附加 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7c939-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7c939-129">新-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7c939-129">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7c939-130">移除-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7c939-130">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7c939-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7c939-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

