---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2c9f006c9e719380abd1f1f5dbb6c6233346a563
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436836"
---
# <span data-ttu-id="21bda-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="21bda-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="21bda-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21bda-102">SYNOPSIS</span></span>
<span data-ttu-id="21bda-103">取得應用程式閘道的私人連結設定。</span><span class="sxs-lookup"><span data-stu-id="21bda-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="21bda-104">句法</span><span class="sxs-lookup"><span data-stu-id="21bda-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21bda-105">說明</span><span class="sxs-lookup"><span data-stu-id="21bda-105">DESCRIPTION</span></span>
<span data-ttu-id="21bda-106">**AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會取得應用程式閘道的私人連結設定。</span><span class="sxs-lookup"><span data-stu-id="21bda-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="21bda-107">示例</span><span class="sxs-lookup"><span data-stu-id="21bda-107">EXAMPLES</span></span>

### <span data-ttu-id="21bda-108">範例1：取得指定的私人連結設定</span><span class="sxs-lookup"><span data-stu-id="21bda-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="21bda-109">第一個命令會從名為 ResourceGroup01 的資源群組中取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="21bda-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="21bda-110">第二個命令會從 $AppGw 取得名為 privateLinkConfig01 的私人連結設定，並將它儲存在 $PrivateLinkConfiguration 變數中。</span><span class="sxs-lookup"><span data-stu-id="21bda-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="21bda-111">範例2：取得私人連結設定清單</span><span class="sxs-lookup"><span data-stu-id="21bda-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="21bda-112">第一個命令會從名為 ResourceGroup01 的資源群組中取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="21bda-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="21bda-113">第二個命令會從 $AppGw 取得所有私人連結設定，並將其儲存在 $PrivateLinkConfigurations 變數中。</span><span class="sxs-lookup"><span data-stu-id="21bda-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="21bda-114">參數</span><span class="sxs-lookup"><span data-stu-id="21bda-114">PARAMETERS</span></span>

### <span data-ttu-id="21bda-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21bda-115">-ApplicationGateway</span></span>
<span data-ttu-id="21bda-116">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21bda-116">The applicationGateway</span></span>

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

### <span data-ttu-id="21bda-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21bda-117">-DefaultProfile</span></span>
<span data-ttu-id="21bda-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21bda-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21bda-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="21bda-119">-Name</span></span>
<span data-ttu-id="21bda-120">應用程式閘道 privateLink 設定的名稱</span><span class="sxs-lookup"><span data-stu-id="21bda-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="21bda-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21bda-121">CommonParameters</span></span>
<span data-ttu-id="21bda-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21bda-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21bda-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="21bda-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21bda-124">輸入</span><span class="sxs-lookup"><span data-stu-id="21bda-124">INPUTS</span></span>

### <span data-ttu-id="21bda-125">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="21bda-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="21bda-126">輸出</span><span class="sxs-lookup"><span data-stu-id="21bda-126">OUTPUTS</span></span>

### <span data-ttu-id="21bda-127">PSApplicationGatewayPrivateLinkConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="21bda-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="21bda-128">筆記</span><span class="sxs-lookup"><span data-stu-id="21bda-128">NOTES</span></span>

## <span data-ttu-id="21bda-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="21bda-129">RELATED LINKS</span></span>

[<span data-ttu-id="21bda-130">新-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="21bda-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="21bda-131">附加 AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="21bda-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="21bda-132">移除-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="21bda-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="21bda-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="21bda-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)