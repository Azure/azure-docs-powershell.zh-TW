---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: a60fa54e5d705a71407f2c56986200c897b838e3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800757"
---
# <span data-ttu-id="1ba36-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1ba36-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1ba36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ba36-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba36-103">從應用程式閘道移除 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="1ba36-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ba36-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ba36-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ba36-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ba36-105">DESCRIPTION</span></span>
<span data-ttu-id="1ba36-106">**AzureRmApplicationGatewayHttpListener** Cmdlet 會從 Azure 應用程式閘道中移除 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="1ba36-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="1ba36-107">示例</span><span class="sxs-lookup"><span data-stu-id="1ba36-107">EXAMPLES</span></span>

### <span data-ttu-id="1ba36-108">範例1：移除應用程式閘道 HTTP 監聽器</span><span class="sxs-lookup"><span data-stu-id="1ba36-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="1ba36-109">第一個命令會取得應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="1ba36-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1ba36-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 Listener02 的 HTTP 偵聽程式。</span><span class="sxs-lookup"><span data-stu-id="1ba36-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="1ba36-111">參數</span><span class="sxs-lookup"><span data-stu-id="1ba36-111">PARAMETERS</span></span>

### <span data-ttu-id="1ba36-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ba36-112">-ApplicationGateway</span></span>
<span data-ttu-id="1ba36-113">指定要從中移除 HTTP 偵聽程式的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="1ba36-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ba36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba36-114">-DefaultProfile</span></span>
<span data-ttu-id="1ba36-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ba36-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba36-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ba36-116">-Name</span></span>
<span data-ttu-id="1ba36-117">指定此 Cmdlet 移除之 HTTP 偵聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ba36-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ba36-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba36-118">CommonParameters</span></span>
<span data-ttu-id="1ba36-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ba36-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba36-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ba36-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba36-121">輸入</span><span class="sxs-lookup"><span data-stu-id="1ba36-121">INPUTS</span></span>

### <span data-ttu-id="1ba36-122">System.object</span><span class="sxs-lookup"><span data-stu-id="1ba36-122">System.String</span></span>

## <span data-ttu-id="1ba36-123">輸出</span><span class="sxs-lookup"><span data-stu-id="1ba36-123">OUTPUTS</span></span>

### <span data-ttu-id="1ba36-124">PSApplicationGatewayHttpListener 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="1ba36-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1ba36-125">筆記</span><span class="sxs-lookup"><span data-stu-id="1ba36-125">NOTES</span></span>

## <span data-ttu-id="1ba36-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ba36-126">RELATED LINKS</span></span>

[<span data-ttu-id="1ba36-127">附加 AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1ba36-127">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1ba36-128">AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1ba36-128">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1ba36-129">新-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1ba36-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1ba36-130">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1ba36-130">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


