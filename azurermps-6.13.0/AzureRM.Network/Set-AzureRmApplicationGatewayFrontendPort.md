---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: 99b4b3272981eafc187eabce0a5669b8975cf91d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455124"
---
# <span data-ttu-id="ed5b5-101">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ed5b5-101">Set-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="ed5b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed5b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5b5-103">修改應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="ed5b5-103">Modifies a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed5b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed5b5-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed5b5-105">說明</span><span class="sxs-lookup"><span data-stu-id="ed5b5-105">DESCRIPTION</span></span>
<span data-ttu-id="ed5b5-106">**AzureRmApplicationGatewayFrontendPort** Cmdlet 會修改應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="ed5b5-106">The **Set-AzureRmApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="ed5b5-107">示例</span><span class="sxs-lookup"><span data-stu-id="ed5b5-107">EXAMPLES</span></span>

### <span data-ttu-id="ed5b5-108">範例1：將應用程式閘道前端埠設定為80</span><span class="sxs-lookup"><span data-stu-id="ed5b5-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="ed5b5-109">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="ed5b5-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ed5b5-110">第二個命令會在 $AppGw 中修改閘道，以將埠80用於名為 FrontEndPort01 的前端埠。</span><span class="sxs-lookup"><span data-stu-id="ed5b5-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="ed5b5-111">參數</span><span class="sxs-lookup"><span data-stu-id="ed5b5-111">PARAMETERS</span></span>

### <span data-ttu-id="ed5b5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed5b5-112">-ApplicationGateway</span></span>
<span data-ttu-id="ed5b5-113">指定此 Cmdlet 將前端埠關聯的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="ed5b5-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="ed5b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5b5-114">-DefaultProfile</span></span>
<span data-ttu-id="ed5b5-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed5b5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed5b5-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed5b5-116">-Name</span></span>
<span data-ttu-id="ed5b5-117">指定要修改的前端埠名稱。</span><span class="sxs-lookup"><span data-stu-id="ed5b5-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="ed5b5-118">-埠</span><span class="sxs-lookup"><span data-stu-id="ed5b5-118">-Port</span></span>
<span data-ttu-id="ed5b5-119">指定要用於前端埠的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="ed5b5-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed5b5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5b5-120">CommonParameters</span></span>
<span data-ttu-id="ed5b5-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed5b5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5b5-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed5b5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5b5-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ed5b5-123">INPUTS</span></span>

### <span data-ttu-id="ed5b5-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ed5b5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="ed5b5-125">參數： ApplicationGateway (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ed5b5-125">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="ed5b5-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ed5b5-126">OUTPUTS</span></span>

### <span data-ttu-id="ed5b5-127">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ed5b5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed5b5-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ed5b5-128">NOTES</span></span>

## <span data-ttu-id="ed5b5-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed5b5-129">RELATED LINKS</span></span>

[<span data-ttu-id="ed5b5-130">附加 AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ed5b5-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ed5b5-131">AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ed5b5-131">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ed5b5-132">新-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ed5b5-132">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="ed5b5-133">移除-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="ed5b5-133">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)
