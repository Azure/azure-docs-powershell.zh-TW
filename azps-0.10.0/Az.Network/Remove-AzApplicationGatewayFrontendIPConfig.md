---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 500d53810050dd539b57d2182a3b1aae9b4f358a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794207"
---
# <span data-ttu-id="fef4c-101">Remove-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fef4c-101">Remove-AzApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="fef4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fef4c-102">SYNOPSIS</span></span>
<span data-ttu-id="fef4c-103">從應用程式閘道移除前端 IP 配置。</span><span class="sxs-lookup"><span data-stu-id="fef4c-103">Removes a front-end IP configuration from an application gateway.</span></span>

## <span data-ttu-id="fef4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="fef4c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fef4c-105">說明</span><span class="sxs-lookup"><span data-stu-id="fef4c-105">DESCRIPTION</span></span>
<span data-ttu-id="fef4c-106">**AzApplicationGatewayFrontendIPConfig** Cmdlet 會將前端 IP 從 Azure 應用程式閘道中移除。</span><span class="sxs-lookup"><span data-stu-id="fef4c-106">The **Remove-AzApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="fef4c-107">示例</span><span class="sxs-lookup"><span data-stu-id="fef4c-107">EXAMPLES</span></span>

### <span data-ttu-id="fef4c-108">範例1：移除前端 IP 設定</span><span class="sxs-lookup"><span data-stu-id="fef4c-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="fef4c-109">第一個命令會取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="fef4c-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="fef4c-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 FrontEndIP02 的前端 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="fef4c-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="fef4c-111">參數</span><span class="sxs-lookup"><span data-stu-id="fef4c-111">PARAMETERS</span></span>

### <span data-ttu-id="fef4c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fef4c-112">-ApplicationGateway</span></span>
<span data-ttu-id="fef4c-113">指定要移除前端 IP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="fef4c-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="fef4c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef4c-114">-DefaultProfile</span></span>
<span data-ttu-id="fef4c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fef4c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fef4c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="fef4c-116">-Name</span></span>
<span data-ttu-id="fef4c-117">指定要移除的前端 IP 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="fef4c-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="fef4c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef4c-118">CommonParameters</span></span>
<span data-ttu-id="fef4c-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fef4c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef4c-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fef4c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef4c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="fef4c-121">INPUTS</span></span>

### <span data-ttu-id="fef4c-122">System.object</span><span class="sxs-lookup"><span data-stu-id="fef4c-122">System.String</span></span>

## <span data-ttu-id="fef4c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="fef4c-123">OUTPUTS</span></span>

### <span data-ttu-id="fef4c-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fef4c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fef4c-125">筆記</span><span class="sxs-lookup"><span data-stu-id="fef4c-125">NOTES</span></span>

## <span data-ttu-id="fef4c-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="fef4c-126">RELATED LINKS</span></span>

[<span data-ttu-id="fef4c-127">附加 AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fef4c-127">Add-AzApplicationGatewayFrontendIPConfig</span></span>](./Add-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fef4c-128">AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fef4c-128">Get-AzApplicationGatewayFrontendIPConfig</span></span>](./Get-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fef4c-129">新-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fef4c-129">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="fef4c-130">Set-AzApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="fef4c-130">Set-AzApplicationGatewayFrontendIPConfig</span></span>](./Set-AzApplicationGatewayFrontendIPConfig.md)


