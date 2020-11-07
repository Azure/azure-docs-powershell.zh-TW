---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: c138ced515932d158bb2a4a067ed405d8084db4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800878"
---
# <span data-ttu-id="3c711-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c711-101">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="3c711-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c711-102">SYNOPSIS</span></span>
<span data-ttu-id="3c711-103">取得應用程式閘道的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="3c711-103">Gets the front-end IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c711-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c711-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c711-105">說明</span><span class="sxs-lookup"><span data-stu-id="3c711-105">DESCRIPTION</span></span>
<span data-ttu-id="3c711-106">**AzureRmApplicationGatewayFrontendIPConfig** Cmdlet 會取得應用程式閘道的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="3c711-106">The **Get-AzureRmApplicationGatewayFrontendIPConfig** cmdlet gets the front-end IP configuration of an application gateway.</span></span>

## <span data-ttu-id="3c711-107">示例</span><span class="sxs-lookup"><span data-stu-id="3c711-107">EXAMPLES</span></span>

### <span data-ttu-id="3c711-108">範例1：取得指定的前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="3c711-108">Example 1: Get a specified front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

<span data-ttu-id="3c711-109">第一個命令會從名為 ResourceGroup01 的資源群組中取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會從 $AppGw 取得名為 FrontEndIP01 的前端 IP 設定，並將它儲存在 $FrontEndIP 變數中。</span><span class="sxs-lookup"><span data-stu-id="3c711-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the front-end IP configuration named FrontEndIP01 from $AppGw and stores it in the $FrontEndIP variable.</span></span>

### <span data-ttu-id="3c711-110">範例2：取得前端 IP 配置清單</span><span class="sxs-lookup"><span data-stu-id="3c711-110">Example 2: Get a list of front-end IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzureRmApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

<span data-ttu-id="3c711-111">第一個命令會從名為 ResourceGroup01 的資源群組中取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會從 $AppGw 取得前端 IP 配置的清單，並將其儲存在 $FrontEndIPs 變數中。</span><span class="sxs-lookup"><span data-stu-id="3c711-111">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets a list of the front-end IP configurations from $AppGw and stores it in the $FrontEndIPs variable.</span></span>

## <span data-ttu-id="3c711-112">參數</span><span class="sxs-lookup"><span data-stu-id="3c711-112">PARAMETERS</span></span>

### <span data-ttu-id="3c711-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c711-113">-ApplicationGateway</span></span>
<span data-ttu-id="3c711-114">指定包含前端 IP 設定的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="3c711-114">Specifies the application gateway object that contains the front-end IP configuration.</span></span>

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

### <span data-ttu-id="3c711-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c711-115">-DefaultProfile</span></span>
<span data-ttu-id="3c711-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c711-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c711-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c711-117">-Name</span></span>
<span data-ttu-id="3c711-118">指定此 Cmdlet 所取得之前端 IP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c711-118">Specifies the name of the front-end IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c711-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c711-119">CommonParameters</span></span>
<span data-ttu-id="3c711-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c711-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c711-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3c711-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c711-122">輸入</span><span class="sxs-lookup"><span data-stu-id="3c711-122">INPUTS</span></span>

### <span data-ttu-id="3c711-123">System.object</span><span class="sxs-lookup"><span data-stu-id="3c711-123">System.String</span></span>

## <span data-ttu-id="3c711-124">輸出</span><span class="sxs-lookup"><span data-stu-id="3c711-124">OUTPUTS</span></span>

### <span data-ttu-id="3c711-125">PSApplicationGatewayFrontendIPConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3c711-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration</span></span>

## <span data-ttu-id="3c711-126">筆記</span><span class="sxs-lookup"><span data-stu-id="3c711-126">NOTES</span></span>

## <span data-ttu-id="3c711-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c711-127">RELATED LINKS</span></span>

[<span data-ttu-id="3c711-128">附加 AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c711-128">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3c711-129">新-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c711-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3c711-130">移除-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c711-130">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Remove-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="3c711-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="3c711-131">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


