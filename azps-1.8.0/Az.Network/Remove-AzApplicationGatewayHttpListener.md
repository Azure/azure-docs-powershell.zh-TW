---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: beceb6788fd2d7498fc886cfbc22aec5ad3a9e23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621661"
---
# <span data-ttu-id="dd3c9-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dd3c9-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="dd3c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="dd3c9-103">從應用程式閘道移除 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="dd3c9-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="dd3c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd3c9-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd3c9-105">說明</span><span class="sxs-lookup"><span data-stu-id="dd3c9-105">DESCRIPTION</span></span>
<span data-ttu-id="dd3c9-106">**AzApplicationGatewayHttpListener** Cmdlet 會從 Azure 應用程式閘道中移除 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="dd3c9-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="dd3c9-107">示例</span><span class="sxs-lookup"><span data-stu-id="dd3c9-107">EXAMPLES</span></span>

### <span data-ttu-id="dd3c9-108">範例1：移除應用程式閘道 HTTP 監聽器</span><span class="sxs-lookup"><span data-stu-id="dd3c9-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="dd3c9-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="dd3c9-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="dd3c9-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 Listener02 的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="dd3c9-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="dd3c9-111">參數</span><span class="sxs-lookup"><span data-stu-id="dd3c9-111">PARAMETERS</span></span>

### <span data-ttu-id="dd3c9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dd3c9-112">-ApplicationGateway</span></span>
<span data-ttu-id="dd3c9-113">指定要從中移除 HTTP 偵聽程式的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="dd3c9-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="dd3c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd3c9-114">-DefaultProfile</span></span>
<span data-ttu-id="dd3c9-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd3c9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd3c9-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd3c9-116">-Name</span></span>
<span data-ttu-id="dd3c9-117">指定此 Cmdlet 移除之 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd3c9-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dd3c9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd3c9-118">CommonParameters</span></span>
<span data-ttu-id="dd3c9-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd3c9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd3c9-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd3c9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd3c9-121">輸入</span><span class="sxs-lookup"><span data-stu-id="dd3c9-121">INPUTS</span></span>

### <span data-ttu-id="dd3c9-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dd3c9-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dd3c9-123">輸出</span><span class="sxs-lookup"><span data-stu-id="dd3c9-123">OUTPUTS</span></span>

### <span data-ttu-id="dd3c9-124">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dd3c9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="dd3c9-125">筆記</span><span class="sxs-lookup"><span data-stu-id="dd3c9-125">NOTES</span></span>

## <span data-ttu-id="dd3c9-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd3c9-126">RELATED LINKS</span></span>

[<span data-ttu-id="dd3c9-127">附加 AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dd3c9-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="dd3c9-128">AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dd3c9-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="dd3c9-129">新-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dd3c9-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="dd3c9-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="dd3c9-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)

