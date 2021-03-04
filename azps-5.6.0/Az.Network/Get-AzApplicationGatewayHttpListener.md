---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e849d4c7eaf007a6e2fd8d6cbbda1cc49cbf2fb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913490"
---
# <span data-ttu-id="1cf4b-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1cf4b-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1cf4b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1cf4b-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf4b-103">獲得應用程式閘道的 HTTP 聆聽者。</span><span class="sxs-lookup"><span data-stu-id="1cf4b-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="1cf4b-104">語法</span><span class="sxs-lookup"><span data-stu-id="1cf4b-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cf4b-105">描述</span><span class="sxs-lookup"><span data-stu-id="1cf4b-105">DESCRIPTION</span></span>
<span data-ttu-id="1cf4b-106">**Get-AzApplicationGatewayHttpListener** Cmdlet 會取得應用程式閘道的 HTTP 聆聽者。</span><span class="sxs-lookup"><span data-stu-id="1cf4b-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="1cf4b-107">例子</span><span class="sxs-lookup"><span data-stu-id="1cf4b-107">EXAMPLES</span></span>

### <span data-ttu-id="1cf4b-108">範例 1：取得特定的 HTTP 聆聽者</span><span class="sxs-lookup"><span data-stu-id="1cf4b-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="1cf4b-109">此命令會獲得一個名為 Listener01 的 HTTP 聆聽者。</span><span class="sxs-lookup"><span data-stu-id="1cf4b-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="1cf4b-110">範例 2：取得 HTTP 聆聽者清單</span><span class="sxs-lookup"><span data-stu-id="1cf4b-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="1cf4b-111">此命令會獲得 HTTP 聆聽者清單。</span><span class="sxs-lookup"><span data-stu-id="1cf4b-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="1cf4b-112">參數</span><span class="sxs-lookup"><span data-stu-id="1cf4b-112">PARAMETERS</span></span>

### <span data-ttu-id="1cf4b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1cf4b-113">-ApplicationGateway</span></span>
<span data-ttu-id="1cf4b-114">指定包含 HTTP 聆聽者的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="1cf4b-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="1cf4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf4b-115">-DefaultProfile</span></span>
<span data-ttu-id="1cf4b-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1cf4b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cf4b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="1cf4b-117">-Name</span></span>
<span data-ttu-id="1cf4b-118">指定此 Cmdlet 所獲得之 HTTP 聆聽者的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cf4b-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="1cf4b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf4b-119">CommonParameters</span></span>
<span data-ttu-id="1cf4b-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1cf4b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf4b-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cf4b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf4b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1cf4b-122">INPUTS</span></span>

### <span data-ttu-id="1cf4b-123">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1cf4b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1cf4b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="1cf4b-124">OUTPUTS</span></span>

### <span data-ttu-id="1cf4b-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1cf4b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1cf4b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="1cf4b-126">NOTES</span></span>

## <span data-ttu-id="1cf4b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cf4b-127">RELATED LINKS</span></span>

[<span data-ttu-id="1cf4b-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1cf4b-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1cf4b-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1cf4b-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1cf4b-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1cf4b-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1cf4b-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1cf4b-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


