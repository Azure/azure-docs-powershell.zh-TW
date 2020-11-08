---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 5aeae0fe7a3efe4513869991d1e53ac429f52401
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139801"
---
# <span data-ttu-id="641a4-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="641a4-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="641a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="641a4-102">SYNOPSIS</span></span>
<span data-ttu-id="641a4-103">取得應用程式閘道的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="641a4-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="641a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="641a4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="641a4-105">說明</span><span class="sxs-lookup"><span data-stu-id="641a4-105">DESCRIPTION</span></span>
<span data-ttu-id="641a4-106">Get-AzApplicationGatewayBackendHttpSetting Cmdlet 會取得應用程式閘道的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="641a4-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="641a4-107">示例</span><span class="sxs-lookup"><span data-stu-id="641a4-107">EXAMPLES</span></span>

### <span data-ttu-id="641a4-108">範例1：依名稱取得後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="641a4-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="641a4-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會針對 $AppGw 取得名為 Settings01 的 HTTP 設定，並將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="641a4-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="641a4-110">範例2：取得後端 HTTP 設定集合</span><span class="sxs-lookup"><span data-stu-id="641a4-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="641a4-111">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會取得 $AppGw 的 HTTP 設定集合，並將設定儲存在 $SettingsList 變數中。</span><span class="sxs-lookup"><span data-stu-id="641a4-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="641a4-112">參數</span><span class="sxs-lookup"><span data-stu-id="641a4-112">PARAMETERS</span></span>

### <span data-ttu-id="641a4-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="641a4-113">-ApplicationGateway</span></span>
<span data-ttu-id="641a4-114">指定包含後端 HTTP 設定的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="641a4-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="641a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="641a4-115">-DefaultProfile</span></span>
<span data-ttu-id="641a4-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="641a4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="641a4-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="641a4-117">-Name</span></span>
<span data-ttu-id="641a4-118">指定此 Cmdlet 所取得之後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="641a4-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="641a4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="641a4-119">CommonParameters</span></span>
<span data-ttu-id="641a4-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="641a4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="641a4-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="641a4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="641a4-122">輸入</span><span class="sxs-lookup"><span data-stu-id="641a4-122">INPUTS</span></span>

### <span data-ttu-id="641a4-123">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="641a4-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="641a4-124">輸出</span><span class="sxs-lookup"><span data-stu-id="641a4-124">OUTPUTS</span></span>

### <span data-ttu-id="641a4-125">PSApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="641a4-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="641a4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="641a4-126">NOTES</span></span>

## <span data-ttu-id="641a4-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="641a4-127">RELATED LINKS</span></span>

[<span data-ttu-id="641a4-128">附加 AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="641a4-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="641a4-129">新-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="641a4-129">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="641a4-130">移除-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="641a4-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="641a4-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="641a4-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

