---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: c9be5f69fc210f68ceb90cfe2e21f5afab164b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452188"
---
# <span data-ttu-id="cb986-101">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cb986-101">Add-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="cb986-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb986-102">SYNOPSIS</span></span>
<span data-ttu-id="cb986-103">將前端埠新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="cb986-103">Adds a front-end port to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb986-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb986-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb986-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb986-105">DESCRIPTION</span></span>
<span data-ttu-id="cb986-106">**AzureRmApplicationGatewayFrontendPort** Cmdlet 會將前端埠新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="cb986-106">The **Add-AzureRmApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="cb986-107">示例</span><span class="sxs-lookup"><span data-stu-id="cb986-107">EXAMPLES</span></span>

### <span data-ttu-id="cb986-108">範例1：將前端埠新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="cb986-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $ AppGw = Add-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="cb986-109">第一個命令會從屬於名為 ResourceGroup01 之資源群組的名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="cb986-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cb986-110">第二個命令會將埠80新增為儲存在 $AppGw 中之應用程式閘道的前端埠，並將埠 FrontEndPort01 命名為。</span><span class="sxs-lookup"><span data-stu-id="cb986-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="cb986-111">參數</span><span class="sxs-lookup"><span data-stu-id="cb986-111">PARAMETERS</span></span>

### <span data-ttu-id="cb986-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cb986-112">-ApplicationGateway</span></span>
<span data-ttu-id="cb986-113">指定此 Cmdlet 新增前端埠的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="cb986-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="cb986-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb986-114">-DefaultProfile</span></span>
<span data-ttu-id="cb986-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb986-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb986-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb986-116">-Name</span></span>
<span data-ttu-id="cb986-117">指定前端埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb986-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="cb986-118">-埠</span><span class="sxs-lookup"><span data-stu-id="cb986-118">-Port</span></span>
<span data-ttu-id="cb986-119">指定埠號碼。</span><span class="sxs-lookup"><span data-stu-id="cb986-119">Specifies the port number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb986-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb986-120">CommonParameters</span></span>
<span data-ttu-id="cb986-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb986-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb986-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb986-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb986-123">輸入</span><span class="sxs-lookup"><span data-stu-id="cb986-123">INPUTS</span></span>

### <span data-ttu-id="cb986-124">System.object</span><span class="sxs-lookup"><span data-stu-id="cb986-124">System.String</span></span>

## <span data-ttu-id="cb986-125">輸出</span><span class="sxs-lookup"><span data-stu-id="cb986-125">OUTPUTS</span></span>

### <span data-ttu-id="cb986-126">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cb986-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cb986-127">筆記</span><span class="sxs-lookup"><span data-stu-id="cb986-127">NOTES</span></span>

## <span data-ttu-id="cb986-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb986-128">RELATED LINKS</span></span>

[<span data-ttu-id="cb986-129">AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cb986-129">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="cb986-130">新-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cb986-130">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="cb986-131">移除-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cb986-131">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="cb986-132">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="cb986-132">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


