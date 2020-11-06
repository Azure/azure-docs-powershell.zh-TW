---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: f0a897dfcc68d2313326d974d1b5a172bd79db6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446750"
---
# <span data-ttu-id="0b35a-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="0b35a-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="0b35a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b35a-102">SYNOPSIS</span></span>
<span data-ttu-id="0b35a-103">取得應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="0b35a-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b35a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b35a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b35a-105">說明</span><span class="sxs-lookup"><span data-stu-id="0b35a-105">DESCRIPTION</span></span>
<span data-ttu-id="0b35a-106">**AzureRmApplicationGatewayFrontendPort** Cmdlet 會取得應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="0b35a-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="0b35a-107">示例</span><span class="sxs-lookup"><span data-stu-id="0b35a-107">EXAMPLES</span></span>

### <span data-ttu-id="0b35a-108">範例1：取得指定的前端埠</span><span class="sxs-lookup"><span data-stu-id="0b35a-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="0b35a-109">第一個命令會從名為 ResourceGroup01 的資源群組中取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="0b35a-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0b35a-110">第二個命令會從 $AppGw 取得名為 FrontEndPort01 的前端埠，並將它儲存在 $FrontEndPort 變數中。</span><span class="sxs-lookup"><span data-stu-id="0b35a-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="0b35a-111">範例2：取得前端埠清單</span><span class="sxs-lookup"><span data-stu-id="0b35a-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="0b35a-112">第一個命令會從名為 ResourceGroup01 的資源群組中取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="0b35a-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0b35a-113">第二個命令會從 $AppGw 取得前端埠清單，並將它儲存在 $FrontEndPorts 變數中。</span><span class="sxs-lookup"><span data-stu-id="0b35a-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="0b35a-114">參數</span><span class="sxs-lookup"><span data-stu-id="0b35a-114">PARAMETERS</span></span>

### <span data-ttu-id="0b35a-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0b35a-115">-ApplicationGateway</span></span>
<span data-ttu-id="0b35a-116">指定包含前端埠的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="0b35a-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="0b35a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b35a-117">-Name</span></span>
<span data-ttu-id="0b35a-118">指定要取得的前端埠名稱。</span><span class="sxs-lookup"><span data-stu-id="0b35a-118">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="0b35a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b35a-119">-DefaultProfile</span></span>
<span data-ttu-id="0b35a-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b35a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b35a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b35a-121">CommonParameters</span></span>
<span data-ttu-id="0b35a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b35a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b35a-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0b35a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b35a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0b35a-124">INPUTS</span></span>

### <span data-ttu-id="0b35a-125">System.object</span><span class="sxs-lookup"><span data-stu-id="0b35a-125">System.String</span></span>

## <span data-ttu-id="0b35a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="0b35a-126">OUTPUTS</span></span>

### <span data-ttu-id="0b35a-127">PSApplicationGatewayFrontendPort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0b35a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="0b35a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="0b35a-128">NOTES</span></span>

## <span data-ttu-id="0b35a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b35a-129">RELATED LINKS</span></span>

[<span data-ttu-id="0b35a-130">附加 AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="0b35a-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="0b35a-131">新-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="0b35a-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="0b35a-132">移除-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="0b35a-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="0b35a-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="0b35a-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


