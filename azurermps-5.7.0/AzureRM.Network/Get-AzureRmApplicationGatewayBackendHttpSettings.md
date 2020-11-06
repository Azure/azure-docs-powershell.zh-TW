---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: f0fa24fd6a7d8ed9cf1a9806ca0a419da8c3deb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449866"
---
# <span data-ttu-id="7f565-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7f565-101">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7f565-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f565-102">SYNOPSIS</span></span>
<span data-ttu-id="7f565-103">取得應用程式閘道的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="7f565-103">Gets the back-end HTTP settings of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f565-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f565-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHttpSettings [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f565-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f565-105">DESCRIPTION</span></span>
<span data-ttu-id="7f565-106">Get-AzureRmApplicationGatewayBackendHttpSettings Cmdlet 會取得應用程式閘道的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="7f565-106">The Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="7f565-107">示例</span><span class="sxs-lookup"><span data-stu-id="7f565-107">EXAMPLES</span></span>

### <span data-ttu-id="7f565-108">範例1：依名稱取得後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="7f565-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="7f565-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會針對 $AppGw 取得名為 Settings01 的 HTTP 設定，並將設定儲存在 $Settings 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f565-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="7f565-110">範例2：取得後端 HTTP 設定集合</span><span class="sxs-lookup"><span data-stu-id="7f565-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw
```

<span data-ttu-id="7f565-111">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會取得 $AppGw 的 HTTP 設定集合，並將設定儲存在 $SettingsList 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f565-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="7f565-112">參數</span><span class="sxs-lookup"><span data-stu-id="7f565-112">PARAMETERS</span></span>

### <span data-ttu-id="7f565-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7f565-113">-ApplicationGateway</span></span>
<span data-ttu-id="7f565-114">指定包含後端 HTTP 設定的應用程式閘道物件。</span><span class="sxs-lookup"><span data-stu-id="7f565-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="7f565-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f565-115">-DefaultProfile</span></span>
<span data-ttu-id="7f565-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f565-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f565-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f565-117">-Name</span></span>
<span data-ttu-id="7f565-118">指定此 Cmdlet 所取得之後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f565-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7f565-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f565-119">CommonParameters</span></span>
<span data-ttu-id="7f565-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f565-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f565-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f565-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f565-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7f565-122">INPUTS</span></span>

### <span data-ttu-id="7f565-123">System.object</span><span class="sxs-lookup"><span data-stu-id="7f565-123">System.String</span></span>

## <span data-ttu-id="7f565-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7f565-124">OUTPUTS</span></span>

### <span data-ttu-id="7f565-125">AzureApplicationGatewayBackendHttpSettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7f565-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7f565-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7f565-126">NOTES</span></span>

## <span data-ttu-id="7f565-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f565-127">RELATED LINKS</span></span>

[<span data-ttu-id="7f565-128">附加 AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7f565-128">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7f565-129">新-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7f565-129">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7f565-130">移除-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7f565-130">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7f565-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7f565-131">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

