---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 4079d8b6859a2860116520c52928d13c7e3fa29e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626370"
---
# <span data-ttu-id="351f1-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="351f1-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="351f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="351f1-102">SYNOPSIS</span></span>
<span data-ttu-id="351f1-103">從應用程式閘道移除 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="351f1-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="351f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="351f1-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="351f1-105">說明</span><span class="sxs-lookup"><span data-stu-id="351f1-105">DESCRIPTION</span></span>
<span data-ttu-id="351f1-106">**AzureRmApplicationGatewayHttpListener** Cmdlet 會從 Azure 應用程式閘道中移除 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="351f1-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="351f1-107">示例</span><span class="sxs-lookup"><span data-stu-id="351f1-107">EXAMPLES</span></span>

### <span data-ttu-id="351f1-108">範例1：移除應用程式閘道 HTTP 監聽器</span><span class="sxs-lookup"><span data-stu-id="351f1-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="351f1-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="351f1-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="351f1-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 Listener02 的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="351f1-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="351f1-111">參數</span><span class="sxs-lookup"><span data-stu-id="351f1-111">PARAMETERS</span></span>

### <span data-ttu-id="351f1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="351f1-112">-ApplicationGateway</span></span>
<span data-ttu-id="351f1-113">指定要從中移除 HTTP 偵聽程式的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="351f1-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="351f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="351f1-114">-DefaultProfile</span></span>
<span data-ttu-id="351f1-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="351f1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="351f1-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="351f1-116">-Name</span></span>
<span data-ttu-id="351f1-117">指定此 Cmdlet 移除之 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="351f1-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="351f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351f1-118">CommonParameters</span></span>
<span data-ttu-id="351f1-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="351f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351f1-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="351f1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351f1-121">輸入</span><span class="sxs-lookup"><span data-stu-id="351f1-121">INPUTS</span></span>

### <span data-ttu-id="351f1-122">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="351f1-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="351f1-123">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="351f1-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="351f1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="351f1-124">OUTPUTS</span></span>

### <span data-ttu-id="351f1-125">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="351f1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="351f1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="351f1-126">NOTES</span></span>

## <span data-ttu-id="351f1-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="351f1-127">RELATED LINKS</span></span>

[<span data-ttu-id="351f1-128">附加 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="351f1-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="351f1-129">AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="351f1-129">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="351f1-130">新-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="351f1-130">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="351f1-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="351f1-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


