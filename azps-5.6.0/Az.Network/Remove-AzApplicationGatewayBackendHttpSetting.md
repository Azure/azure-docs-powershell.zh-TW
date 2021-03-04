---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 24c3a0264250bf9defc8be8b046f48ea94f28244
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902866"
---
# <span data-ttu-id="5fee4-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5fee4-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="5fee4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5fee4-102">SYNOPSIS</span></span>
<span data-ttu-id="5fee4-103">從應用程式閘道移除後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="5fee4-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="5fee4-104">語法</span><span class="sxs-lookup"><span data-stu-id="5fee4-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fee4-105">描述</span><span class="sxs-lookup"><span data-stu-id="5fee4-105">DESCRIPTION</span></span>
<span data-ttu-id="5fee4-106">Cmdlet Remove-AzApplicationGatewayBackendHttpSetting從 Azure 應用程式閘道移除後端超文字傳輸通訊協定 (HTTP) 設定。</span><span class="sxs-lookup"><span data-stu-id="5fee4-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="5fee4-107">例子</span><span class="sxs-lookup"><span data-stu-id="5fee4-107">EXAMPLES</span></span>

### <span data-ttu-id="5fee4-108">範例 1：從應用程式閘道移除後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="5fee4-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="5fee4-109">第一個命令會獲得名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並儲存在$AppGw變數中。</span><span class="sxs-lookup"><span data-stu-id="5fee4-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5fee4-110">第二個命令會從儲存在 $AppGw 的應用程式閘道移除名為 BackEndSetting02 的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="5fee4-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="5fee4-111">參數</span><span class="sxs-lookup"><span data-stu-id="5fee4-111">PARAMETERS</span></span>

### <span data-ttu-id="5fee4-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5fee4-112">-ApplicationGateway</span></span>
<span data-ttu-id="5fee4-113">指定此 Cmdlet 會移除後端 HTTP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5fee4-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="5fee4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fee4-114">-DefaultProfile</span></span>
<span data-ttu-id="5fee4-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5fee4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fee4-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="5fee4-116">-Name</span></span>
<span data-ttu-id="5fee4-117">指定此 Cmdlet 移除的後端 HTTP 設定名稱。</span><span class="sxs-lookup"><span data-stu-id="5fee4-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5fee4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fee4-118">CommonParameters</span></span>
<span data-ttu-id="5fee4-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5fee4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fee4-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5fee4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fee4-121">輸入</span><span class="sxs-lookup"><span data-stu-id="5fee4-121">INPUTS</span></span>

### <span data-ttu-id="5fee4-122">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5fee4-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5fee4-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5fee4-123">OUTPUTS</span></span>

### <span data-ttu-id="5fee4-124">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5fee4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5fee4-125">筆記</span><span class="sxs-lookup"><span data-stu-id="5fee4-125">NOTES</span></span>

## <span data-ttu-id="5fee4-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="5fee4-126">RELATED LINKS</span></span>

[<span data-ttu-id="5fee4-127">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5fee4-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5fee4-128">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5fee4-128">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5fee4-129">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5fee4-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5fee4-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5fee4-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

