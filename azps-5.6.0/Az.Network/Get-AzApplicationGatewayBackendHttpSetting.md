---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 957417d7751080a82ddc8785abdd124c8f723303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915357"
---
# <span data-ttu-id="2b149-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2b149-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="2b149-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2b149-102">SYNOPSIS</span></span>
<span data-ttu-id="2b149-103">獲得應用程式閘道的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="2b149-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="2b149-104">語法</span><span class="sxs-lookup"><span data-stu-id="2b149-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b149-105">描述</span><span class="sxs-lookup"><span data-stu-id="2b149-105">DESCRIPTION</span></span>
<span data-ttu-id="2b149-106">Cmdlet Get-AzApplicationGatewayBackendHttpSetting Cmdlet 會獲得應用程式閘道的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="2b149-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="2b149-107">例子</span><span class="sxs-lookup"><span data-stu-id="2b149-107">EXAMPLES</span></span>

### <span data-ttu-id="2b149-108">範例 1：按名稱取得後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="2b149-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="2b149-109">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在 $AppGw 變數中。第二個命令會獲得名稱為 Settings01 的 HTTP 設定$AppGw將設定儲存在$Settings變數中。</span><span class="sxs-lookup"><span data-stu-id="2b149-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="2b149-110">範例 2：取得後端 HTTP 設定的集合</span><span class="sxs-lookup"><span data-stu-id="2b149-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="2b149-111">第一個命令會獲得名為 ResourceGroup01 的資源群組中名為 ApplicationGateway01 的應用程式閘道，並儲存在 $AppGw 變數中。第二個命令會收集您$AppGw HTTP 設定，並儲存在$SettingsList變數中。</span><span class="sxs-lookup"><span data-stu-id="2b149-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="2b149-112">參數</span><span class="sxs-lookup"><span data-stu-id="2b149-112">PARAMETERS</span></span>

### <span data-ttu-id="2b149-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b149-113">-ApplicationGateway</span></span>
<span data-ttu-id="2b149-114">指定包含後端 HTTP 設定的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="2b149-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="2b149-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b149-115">-DefaultProfile</span></span>
<span data-ttu-id="2b149-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b149-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b149-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b149-117">-Name</span></span>
<span data-ttu-id="2b149-118">指定此 Cmdlet 所獲得後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b149-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2b149-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b149-119">CommonParameters</span></span>
<span data-ttu-id="2b149-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2b149-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b149-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b149-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b149-122">輸入</span><span class="sxs-lookup"><span data-stu-id="2b149-122">INPUTS</span></span>

### <span data-ttu-id="2b149-123">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2b149-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2b149-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2b149-124">OUTPUTS</span></span>

### <span data-ttu-id="2b149-125">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2b149-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2b149-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2b149-126">NOTES</span></span>

## <span data-ttu-id="2b149-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b149-127">RELATED LINKS</span></span>

[<span data-ttu-id="2b149-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2b149-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2b149-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2b149-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2b149-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2b149-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2b149-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2b149-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

