---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 168223e9e442b7aa37da11f3a1e0a092c3cb3efc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794211"
---
# <span data-ttu-id="511ff-101">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="511ff-101">Remove-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="511ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="511ff-102">SYNOPSIS</span></span>
<span data-ttu-id="511ff-103">從應用程式閘道移除後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="511ff-103">Removes back-end HTTP settings from an application gateway.</span></span>

## <span data-ttu-id="511ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="511ff-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayBackendHttpSetting -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="511ff-105">說明</span><span class="sxs-lookup"><span data-stu-id="511ff-105">DESCRIPTION</span></span>
<span data-ttu-id="511ff-106">Remove-AzApplicationGatewayBackendHttpSetting Cmdlet 會從 Azure 應用程式閘道 (HTTP) 設定中移除後端超文字傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="511ff-106">The Remove-AzApplicationGatewayBackendHttpSetting cmdlet removes back-end Hypertext Transfer Protocol (HTTP) settings from an Azure application gateway.</span></span>

## <span data-ttu-id="511ff-107">示例</span><span class="sxs-lookup"><span data-stu-id="511ff-107">EXAMPLES</span></span>

### <span data-ttu-id="511ff-108">範例1：從應用程式閘道移除後端 HTTP 設定</span><span class="sxs-lookup"><span data-stu-id="511ff-108">Example 1: Remove back-end HTTP settings from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "BackEndSetting02"
```

<span data-ttu-id="511ff-109">第一個命令會取得一個名為 ApplicationGateway01 的應用程式閘道，該閘道屬於名為 ResourceGroup01 的資源群組，並將它儲存在 $AppGw 變數中。</span><span class="sxs-lookup"><span data-stu-id="511ff-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="511ff-110">第二個命令會從儲存在 $AppGw 的應用程式閘道中，移除名為 BackEndSetting02 的後端 HTTP 設定。</span><span class="sxs-lookup"><span data-stu-id="511ff-110">The second command removes the back-end HTTP setting named BackEndSetting02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="511ff-111">參數</span><span class="sxs-lookup"><span data-stu-id="511ff-111">PARAMETERS</span></span>

### <span data-ttu-id="511ff-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="511ff-112">-ApplicationGateway</span></span>
<span data-ttu-id="511ff-113">指定此 Cmdlet 移除後端 HTTP 設定的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="511ff-113">Specifies the application gateway from which this cmdlet removes back-end HTTP settings.</span></span>

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

### <span data-ttu-id="511ff-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="511ff-114">-DefaultProfile</span></span>
<span data-ttu-id="511ff-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="511ff-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="511ff-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="511ff-116">-Name</span></span>
<span data-ttu-id="511ff-117">指定此 Cmdlet 移除之後端 HTTP 設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="511ff-117">Specifies the name of the back-end HTTP settings that this cmdlet removes.</span></span>

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

### <span data-ttu-id="511ff-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="511ff-118">CommonParameters</span></span>
<span data-ttu-id="511ff-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="511ff-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="511ff-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="511ff-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="511ff-121">輸入</span><span class="sxs-lookup"><span data-stu-id="511ff-121">INPUTS</span></span>

### <span data-ttu-id="511ff-122">System.object</span><span class="sxs-lookup"><span data-stu-id="511ff-122">System.String</span></span>

## <span data-ttu-id="511ff-123">輸出</span><span class="sxs-lookup"><span data-stu-id="511ff-123">OUTPUTS</span></span>

### <span data-ttu-id="511ff-124">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="511ff-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="511ff-125">筆記</span><span class="sxs-lookup"><span data-stu-id="511ff-125">NOTES</span></span>

## <span data-ttu-id="511ff-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="511ff-126">RELATED LINKS</span></span>

[<span data-ttu-id="511ff-127">附加 AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="511ff-127">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="511ff-128">新-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="511ff-128">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="511ff-129">AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="511ff-129">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="511ff-130">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="511ff-130">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

