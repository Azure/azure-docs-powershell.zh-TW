---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 0cb29f9ad00c2412d9ab492bba780e977ef6b571
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626083"
---
# <span data-ttu-id="fe9b3-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe9b3-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="fe9b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9b3-103">取得應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="fe9b3-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe9b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe9b3-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe9b3-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe9b3-105">DESCRIPTION</span></span>
<span data-ttu-id="fe9b3-106">**AzureRmApplicationGatewayHttpListener** Cmdlet 會取得應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="fe9b3-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="fe9b3-107">示例</span><span class="sxs-lookup"><span data-stu-id="fe9b3-107">EXAMPLES</span></span>

### <span data-ttu-id="fe9b3-108">範例1：取得特定的 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="fe9b3-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="fe9b3-109">這個命令會取得名為 Listener01 的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="fe9b3-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="fe9b3-110">範例2：取得 HTTP 偵聽程式清單</span><span class="sxs-lookup"><span data-stu-id="fe9b3-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="fe9b3-111">這個命令會取得 HTTP 偵聽程式的清單。</span><span class="sxs-lookup"><span data-stu-id="fe9b3-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="fe9b3-112">參數</span><span class="sxs-lookup"><span data-stu-id="fe9b3-112">PARAMETERS</span></span>

### <span data-ttu-id="fe9b3-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fe9b3-113">-ApplicationGateway</span></span>
<span data-ttu-id="fe9b3-114">指定包含 HTTP 偵聽程式的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="fe9b3-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="fe9b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9b3-115">-DefaultProfile</span></span>
<span data-ttu-id="fe9b3-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe9b3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe9b3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe9b3-117">-Name</span></span>
<span data-ttu-id="fe9b3-118">指定此 Cmdlet 所取得之 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe9b3-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="fe9b3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9b3-119">CommonParameters</span></span>
<span data-ttu-id="fe9b3-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe9b3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9b3-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe9b3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9b3-122">輸入</span><span class="sxs-lookup"><span data-stu-id="fe9b3-122">INPUTS</span></span>

### <span data-ttu-id="fe9b3-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fe9b3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="fe9b3-124">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="fe9b3-124">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="fe9b3-125">輸出</span><span class="sxs-lookup"><span data-stu-id="fe9b3-125">OUTPUTS</span></span>

### <span data-ttu-id="fe9b3-126">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fe9b3-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="fe9b3-127">筆記</span><span class="sxs-lookup"><span data-stu-id="fe9b3-127">NOTES</span></span>

## <span data-ttu-id="fe9b3-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe9b3-128">RELATED LINKS</span></span>

[<span data-ttu-id="fe9b3-129">附加 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe9b3-129">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="fe9b3-130">新-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe9b3-130">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="fe9b3-131">移除-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe9b3-131">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="fe9b3-132">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="fe9b3-132">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


