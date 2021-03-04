---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 4b28feb85ebc8f4d5669f28609aa4723061c1709
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912346"
---
# <span data-ttu-id="af52c-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="af52c-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="af52c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="af52c-102">SYNOPSIS</span></span>
<span data-ttu-id="af52c-103">從應用程式閘道移除前端埠。</span><span class="sxs-lookup"><span data-stu-id="af52c-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="af52c-104">語法</span><span class="sxs-lookup"><span data-stu-id="af52c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af52c-105">描述</span><span class="sxs-lookup"><span data-stu-id="af52c-105">DESCRIPTION</span></span>
<span data-ttu-id="af52c-106">**Remove-AzApplicationGatewayFrontendPort** Cmdlet 會從 Azure 應用程式閘道移除前端埠。</span><span class="sxs-lookup"><span data-stu-id="af52c-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="af52c-107">例子</span><span class="sxs-lookup"><span data-stu-id="af52c-107">EXAMPLES</span></span>

### <span data-ttu-id="af52c-108">範例：從應用程式閘道移除前端埠</span><span class="sxs-lookup"><span data-stu-id="af52c-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="af52c-109">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，它屬於名為 ResourceGroup01 的資源群組，並且將閘道儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="af52c-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="af52c-110">第二個命令會從應用程式閘道移除名為 FrontEndPort02 的埠。</span><span class="sxs-lookup"><span data-stu-id="af52c-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="af52c-111">參數</span><span class="sxs-lookup"><span data-stu-id="af52c-111">PARAMETERS</span></span>

### <span data-ttu-id="af52c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af52c-112">-ApplicationGateway</span></span>
<span data-ttu-id="af52c-113">指定要從中移除前端埠的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="af52c-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="af52c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af52c-114">-DefaultProfile</span></span>
<span data-ttu-id="af52c-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="af52c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af52c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="af52c-116">-Name</span></span>
<span data-ttu-id="af52c-117">指定要移除的前端埠名稱。</span><span class="sxs-lookup"><span data-stu-id="af52c-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="af52c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af52c-118">CommonParameters</span></span>
<span data-ttu-id="af52c-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="af52c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af52c-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="af52c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af52c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="af52c-121">INPUTS</span></span>

### <span data-ttu-id="af52c-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af52c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="af52c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="af52c-123">OUTPUTS</span></span>

### <span data-ttu-id="af52c-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="af52c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="af52c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="af52c-125">NOTES</span></span>

## <span data-ttu-id="af52c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="af52c-126">RELATED LINKS</span></span>

[<span data-ttu-id="af52c-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="af52c-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="af52c-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="af52c-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="af52c-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="af52c-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="af52c-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="af52c-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


