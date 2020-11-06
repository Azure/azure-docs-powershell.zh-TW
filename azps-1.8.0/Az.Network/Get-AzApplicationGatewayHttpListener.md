---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 91b2791b7f61c7586c1fbd4bca954e374ccbb43c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622094"
---
# <span data-ttu-id="a0af1-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a0af1-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a0af1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0af1-102">SYNOPSIS</span></span>
<span data-ttu-id="a0af1-103">取得應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="a0af1-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="a0af1-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0af1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0af1-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0af1-105">DESCRIPTION</span></span>
<span data-ttu-id="a0af1-106">**AzApplicationGatewayHttpListener** Cmdlet 會取得應用程式閘道的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="a0af1-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="a0af1-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0af1-107">EXAMPLES</span></span>

### <span data-ttu-id="a0af1-108">範例1：取得特定的 HTTP 偵聽程式</span><span class="sxs-lookup"><span data-stu-id="a0af1-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="a0af1-109">這個命令會取得名為 Listener01 的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="a0af1-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="a0af1-110">範例2：取得 HTTP 偵聽程式清單</span><span class="sxs-lookup"><span data-stu-id="a0af1-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="a0af1-111">這個命令會取得 HTTP 偵聽程式的清單。</span><span class="sxs-lookup"><span data-stu-id="a0af1-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="a0af1-112">參數</span><span class="sxs-lookup"><span data-stu-id="a0af1-112">PARAMETERS</span></span>

### <span data-ttu-id="a0af1-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a0af1-113">-ApplicationGateway</span></span>
<span data-ttu-id="a0af1-114">指定包含 HTTP 偵聽程式的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="a0af1-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="a0af1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0af1-115">-DefaultProfile</span></span>
<span data-ttu-id="a0af1-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0af1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0af1-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0af1-117">-Name</span></span>
<span data-ttu-id="a0af1-118">指定此 Cmdlet 所取得之 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0af1-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="a0af1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0af1-119">CommonParameters</span></span>
<span data-ttu-id="a0af1-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0af1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0af1-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0af1-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0af1-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a0af1-122">INPUTS</span></span>

### <span data-ttu-id="a0af1-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a0af1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a0af1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a0af1-124">OUTPUTS</span></span>

### <span data-ttu-id="a0af1-125">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a0af1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a0af1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a0af1-126">NOTES</span></span>

## <span data-ttu-id="a0af1-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0af1-127">RELATED LINKS</span></span>

[<span data-ttu-id="a0af1-128">附加 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a0af1-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a0af1-129">新-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a0af1-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a0af1-130">移除-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a0af1-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a0af1-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a0af1-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


