---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: bb37c72368832ee4bbccb6e4c10a227e72ba127f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790713"
---
# <span data-ttu-id="4348b-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4348b-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="4348b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4348b-102">SYNOPSIS</span></span>
<span data-ttu-id="4348b-103">從應用程式閘道移除前端埠。</span><span class="sxs-lookup"><span data-stu-id="4348b-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="4348b-104">句法</span><span class="sxs-lookup"><span data-stu-id="4348b-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4348b-105">說明</span><span class="sxs-lookup"><span data-stu-id="4348b-105">DESCRIPTION</span></span>
<span data-ttu-id="4348b-106">**AzApplicationGatewayFrontendPort** Cmdlet 會將前端埠從 Azure 應用程式閘道中移除。</span><span class="sxs-lookup"><span data-stu-id="4348b-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="4348b-107">示例</span><span class="sxs-lookup"><span data-stu-id="4348b-107">EXAMPLES</span></span>

### <span data-ttu-id="4348b-108">範例：從應用程式閘道移除前端埠</span><span class="sxs-lookup"><span data-stu-id="4348b-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="4348b-109">第一個命令會取得一個名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並將閘道儲存 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="4348b-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>
<span data-ttu-id="4348b-110">第二個命令會從應用程式閘道移除名為 FrontEndPort02 的埠。</span><span class="sxs-lookup"><span data-stu-id="4348b-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="4348b-111">參數</span><span class="sxs-lookup"><span data-stu-id="4348b-111">PARAMETERS</span></span>

### <span data-ttu-id="4348b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4348b-112">-ApplicationGateway</span></span>
<span data-ttu-id="4348b-113">指定要移除前端埠的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="4348b-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="4348b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4348b-114">-DefaultProfile</span></span>
<span data-ttu-id="4348b-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4348b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4348b-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="4348b-116">-Name</span></span>
<span data-ttu-id="4348b-117">指定要移除之前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="4348b-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="4348b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4348b-118">CommonParameters</span></span>
<span data-ttu-id="4348b-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4348b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4348b-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4348b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4348b-121">輸入</span><span class="sxs-lookup"><span data-stu-id="4348b-121">INPUTS</span></span>

### <span data-ttu-id="4348b-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4348b-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4348b-123">輸出</span><span class="sxs-lookup"><span data-stu-id="4348b-123">OUTPUTS</span></span>

### <span data-ttu-id="4348b-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4348b-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4348b-125">筆記</span><span class="sxs-lookup"><span data-stu-id="4348b-125">NOTES</span></span>

## <span data-ttu-id="4348b-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="4348b-126">RELATED LINKS</span></span>

[<span data-ttu-id="4348b-127">附加 AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4348b-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4348b-128">AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4348b-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4348b-129">新-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4348b-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4348b-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4348b-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)

