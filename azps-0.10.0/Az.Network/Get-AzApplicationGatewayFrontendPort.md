---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: be1e70538aae66b05bdff5b06859cfb2f30681ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794468"
---
# <span data-ttu-id="7f431-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7f431-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="7f431-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f431-102">SYNOPSIS</span></span>
<span data-ttu-id="7f431-103">取得應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="7f431-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="7f431-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f431-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f431-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f431-105">DESCRIPTION</span></span>
<span data-ttu-id="7f431-106">**AzApplicationGatewayFrontendPort** Cmdlet 會取得應用程式閘道的前端埠。</span><span class="sxs-lookup"><span data-stu-id="7f431-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="7f431-107">示例</span><span class="sxs-lookup"><span data-stu-id="7f431-107">EXAMPLES</span></span>

### <span data-ttu-id="7f431-108">範例1：取得指定的前端埠</span><span class="sxs-lookup"><span data-stu-id="7f431-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="7f431-109">第一個命令會從名為 ResourceGroup01 的資源群組中取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f431-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7f431-110">第二個命令會從 $AppGw 取得名為 FrontEndPort01 的前端埠，並將它儲存在 $FrontEndPort 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f431-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="7f431-111">範例2：取得前端埠清單</span><span class="sxs-lookup"><span data-stu-id="7f431-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="7f431-112">第一個命令會從名為 ResourceGroup01 的資源群組中取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f431-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7f431-113">第二個命令會從 $AppGw 取得前端埠清單，並將它儲存在 $FrontEndPorts 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f431-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="7f431-114">參數</span><span class="sxs-lookup"><span data-stu-id="7f431-114">PARAMETERS</span></span>

### <span data-ttu-id="7f431-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f431-115">-ApplicationGateway</span></span>
<span data-ttu-id="7f431-116">指定包含前端埠的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="7f431-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="7f431-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f431-117">-DefaultProfile</span></span>
<span data-ttu-id="7f431-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f431-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f431-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f431-119">-Name</span></span>
<span data-ttu-id="7f431-120">指定要取得的前端埠名稱。</span><span class="sxs-lookup"><span data-stu-id="7f431-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="7f431-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f431-121">CommonParameters</span></span>
<span data-ttu-id="7f431-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f431-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f431-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f431-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f431-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7f431-124">INPUTS</span></span>

### <span data-ttu-id="7f431-125">System.object</span><span class="sxs-lookup"><span data-stu-id="7f431-125">System.String</span></span>

## <span data-ttu-id="7f431-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7f431-126">OUTPUTS</span></span>

### <span data-ttu-id="7f431-127">PSApplicationGatewayFrontendPort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7f431-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="7f431-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7f431-128">NOTES</span></span>

## <span data-ttu-id="7f431-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f431-129">RELATED LINKS</span></span>

[<span data-ttu-id="7f431-130">附加 AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7f431-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7f431-131">新-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7f431-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7f431-132">移除-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7f431-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="7f431-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="7f431-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


