---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 46cf3a786642262c1f6d0df0e2c1fd770d61ec6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903794"
---
# <span data-ttu-id="db529-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db529-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="db529-102">簡介</span><span class="sxs-lookup"><span data-stu-id="db529-102">SYNOPSIS</span></span>
<span data-ttu-id="db529-103">從應用程式閘道移除 HTTP 聆聽者。</span><span class="sxs-lookup"><span data-stu-id="db529-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="db529-104">語法</span><span class="sxs-lookup"><span data-stu-id="db529-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db529-105">描述</span><span class="sxs-lookup"><span data-stu-id="db529-105">DESCRIPTION</span></span>
<span data-ttu-id="db529-106">**Remove-AzApplicationGatewayHttpListener** Cmdlet 會從 Azure 應用程式閘道移除 HTTP 聆聽者。</span><span class="sxs-lookup"><span data-stu-id="db529-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="db529-107">例子</span><span class="sxs-lookup"><span data-stu-id="db529-107">EXAMPLES</span></span>

### <span data-ttu-id="db529-108">範例 1：移除應用程式閘道 HTTP 聆聽者</span><span class="sxs-lookup"><span data-stu-id="db529-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="db529-109">第一個命令會獲得應用程式閘道，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="db529-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="db529-110">第二個命令會從儲存在 $AppGw 的應用程式閘道移除名為 Listener02 的 HTTP $AppGw。</span><span class="sxs-lookup"><span data-stu-id="db529-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="db529-111">參數</span><span class="sxs-lookup"><span data-stu-id="db529-111">PARAMETERS</span></span>

### <span data-ttu-id="db529-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db529-112">-ApplicationGateway</span></span>
<span data-ttu-id="db529-113">指定要從中移除 HTTP 聆聽者的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="db529-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="db529-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db529-114">-DefaultProfile</span></span>
<span data-ttu-id="db529-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="db529-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db529-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="db529-116">-Name</span></span>
<span data-ttu-id="db529-117">指定此 Cmdlet 移除的 HTTP 聆聽者名稱。</span><span class="sxs-lookup"><span data-stu-id="db529-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db529-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db529-118">CommonParameters</span></span>
<span data-ttu-id="db529-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="db529-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db529-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="db529-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db529-121">輸入</span><span class="sxs-lookup"><span data-stu-id="db529-121">INPUTS</span></span>

### <span data-ttu-id="db529-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db529-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="db529-123">輸出</span><span class="sxs-lookup"><span data-stu-id="db529-123">OUTPUTS</span></span>

### <span data-ttu-id="db529-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db529-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="db529-125">筆記</span><span class="sxs-lookup"><span data-stu-id="db529-125">NOTES</span></span>

## <span data-ttu-id="db529-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="db529-126">RELATED LINKS</span></span>

[<span data-ttu-id="db529-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db529-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="db529-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db529-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="db529-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db529-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="db529-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="db529-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


