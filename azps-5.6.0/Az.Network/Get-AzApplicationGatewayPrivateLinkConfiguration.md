---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: d3f774b078c1069fc5a2c2690996837f17a4c187
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912794"
---
# <span data-ttu-id="7f52e-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f52e-101">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="7f52e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7f52e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f52e-103">獲得應用程式閘道的私人連結組。</span><span class="sxs-lookup"><span data-stu-id="7f52e-103">Gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="7f52e-104">語法</span><span class="sxs-lookup"><span data-stu-id="7f52e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f52e-105">描述</span><span class="sxs-lookup"><span data-stu-id="7f52e-105">DESCRIPTION</span></span>
<span data-ttu-id="7f52e-106">**Get-AzApplicationGatewayPrivateLinkConfiguration** Cmdlet 會取得應用程式閘道的私人連結組式。</span><span class="sxs-lookup"><span data-stu-id="7f52e-106">The **Get-AzApplicationGatewayPrivateLinkConfiguration** cmdlet gets the private link configuration of an application gateway.</span></span>

## <span data-ttu-id="7f52e-107">例子</span><span class="sxs-lookup"><span data-stu-id="7f52e-107">EXAMPLES</span></span>

### <span data-ttu-id="7f52e-108">範例 1：取得指定的私人連結組</span><span class="sxs-lookup"><span data-stu-id="7f52e-108">Example 1 : Get a specified private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfiguration = Get-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -ApplicationGateway $AppGw
```

<span data-ttu-id="7f52e-109">第一個命令會從名為 ResourceGroup01 的資源群組中，獲得名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="7f52e-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7f52e-110">第二個命令會從命令中$AppGw名為 privateLinkConfig01 的私人連結組$PrivateLinkConfiguration變數。</span><span class="sxs-lookup"><span data-stu-id="7f52e-110">The second command gets the private link configuration named privateLinkConfig01 from $AppGw and stores it in the $PrivateLinkConfiguration variable.</span></span>

### <span data-ttu-id="7f52e-111">範例 2：取得私人連結組配置清單</span><span class="sxs-lookup"><span data-stu-id="7f52e-111">Example 2 : Get a list of private link configuration</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $PrivateLinkConfigurations = Get-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="7f52e-112">第一個命令會從名為 ResourceGroup01 的資源群組中，獲得名為 ApplicationGateway01 的應用程式閘道，並儲存在$AppGw變數。</span><span class="sxs-lookup"><span data-stu-id="7f52e-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7f52e-113">第二個命令會從 $AppGw 中獲得所有私人連結組$PrivateLinkConfigurations變數。</span><span class="sxs-lookup"><span data-stu-id="7f52e-113">The second command gets all the private link configurations from $AppGw and stores it in the $PrivateLinkConfigurations variable.</span></span>

## <span data-ttu-id="7f52e-114">參數</span><span class="sxs-lookup"><span data-stu-id="7f52e-114">PARAMETERS</span></span>

### <span data-ttu-id="7f52e-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f52e-115">-ApplicationGateway</span></span>
<span data-ttu-id="7f52e-116">應用程式Gateway</span><span class="sxs-lookup"><span data-stu-id="7f52e-116">The applicationGateway</span></span>

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

### <span data-ttu-id="7f52e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f52e-117">-DefaultProfile</span></span>
<span data-ttu-id="7f52e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f52e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f52e-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f52e-119">-Name</span></span>
<span data-ttu-id="7f52e-120">應用程式閘道 privateLink 組組的名稱</span><span class="sxs-lookup"><span data-stu-id="7f52e-120">The name of the application gateway privateLink configuration</span></span>

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

### <span data-ttu-id="7f52e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f52e-121">CommonParameters</span></span>
<span data-ttu-id="7f52e-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7f52e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f52e-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f52e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f52e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7f52e-124">INPUTS</span></span>

### <span data-ttu-id="7f52e-125">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f52e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7f52e-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7f52e-126">OUTPUTS</span></span>

### <span data-ttu-id="7f52e-127">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f52e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="7f52e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7f52e-128">NOTES</span></span>

## <span data-ttu-id="7f52e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f52e-129">RELATED LINKS</span></span>

[<span data-ttu-id="7f52e-130">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f52e-130">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7f52e-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f52e-131">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7f52e-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f52e-132">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="7f52e-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7f52e-133">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)