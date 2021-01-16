---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 6d4bab8f7c4c766730dd6fb09f0d0a011d5d3739
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277852"
---
# <span data-ttu-id="4bcb3-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="4bcb3-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="4bcb3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bcb3-102">SYNOPSIS</span></span>
<span data-ttu-id="4bcb3-103">取得應用程式閘道的 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4bcb3-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="4bcb3-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bcb3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bcb3-105">說明</span><span class="sxs-lookup"><span data-stu-id="4bcb3-105">DESCRIPTION</span></span>
<span data-ttu-id="4bcb3-106">**AzApplicationGatewaySslProfile** Cmdlet 會取得應用程式閘道的 SSL 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4bcb3-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="4bcb3-107">示例</span><span class="sxs-lookup"><span data-stu-id="4bcb3-107">EXAMPLES</span></span>

### <span data-ttu-id="4bcb3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4bcb3-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="4bcb3-109">第一個命令會在名為 ResourceGroup01 的資源群組中，取得名為 ApplicationGateway01 的應用程式閘道，並將它儲存在 $AppGw 變數中。第二個命令會取得 $AppGw 的 SSL 設定檔 SslProfile01，並將它儲存在 $profile 變數中。</span><span class="sxs-lookup"><span data-stu-id="4bcb3-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="4bcb3-110">參數</span><span class="sxs-lookup"><span data-stu-id="4bcb3-110">PARAMETERS</span></span>

### <span data-ttu-id="4bcb3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bcb3-111">-ApplicationGateway</span></span>
<span data-ttu-id="4bcb3-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bcb3-112">The applicationGateway</span></span>

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

### <span data-ttu-id="4bcb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bcb3-113">-DefaultProfile</span></span>
<span data-ttu-id="4bcb3-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bcb3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bcb3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bcb3-115">-Name</span></span>
<span data-ttu-id="4bcb3-116">Ssl 設定檔的名稱</span><span class="sxs-lookup"><span data-stu-id="4bcb3-116">The name of the ssl profile</span></span>

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

### <span data-ttu-id="4bcb3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bcb3-117">CommonParameters</span></span>
<span data-ttu-id="4bcb3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bcb3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bcb3-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4bcb3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bcb3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4bcb3-120">INPUTS</span></span>

### <span data-ttu-id="4bcb3-121">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4bcb3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4bcb3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="4bcb3-122">OUTPUTS</span></span>

### <span data-ttu-id="4bcb3-123">PSApplicationGatewaySslProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4bcb3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="4bcb3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="4bcb3-124">NOTES</span></span>

## <span data-ttu-id="4bcb3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bcb3-125">RELATED LINKS</span></span>

[<span data-ttu-id="4bcb3-126">新-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="4bcb3-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="4bcb3-127">附加 AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="4bcb3-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="4bcb3-128">移除-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="4bcb3-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="4bcb3-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="4bcb3-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)