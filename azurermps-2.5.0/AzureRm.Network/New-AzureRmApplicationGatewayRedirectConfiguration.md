---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 2cb7455d5a902882fdd98dd5fea47ae5a28e1dc9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799786"
---
# <span data-ttu-id="f4a1e-101">New-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4a1e-101">New-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="f4a1e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4a1e-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a1e-103">建立應用程式閘道的重新導向設定。</span><span class="sxs-lookup"><span data-stu-id="f4a1e-103">Creates a redirect configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4a1e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4a1e-104">SYNTAX</span></span>

### <span data-ttu-id="f4a1e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4a1e-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListenerID <String>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4a1e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f4a1e-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String>
 [-TargetListener <PSApplicationGatewayHttpListener>] [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4a1e-107">SetByURL</span><span class="sxs-lookup"><span data-stu-id="f4a1e-107">SetByURL</span></span>
```
New-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -RedirectType <String> [-TargetUrl <String>]
 [-IncludePath <Boolean>] [-IncludeQueryString <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4a1e-108">說明</span><span class="sxs-lookup"><span data-stu-id="f4a1e-108">DESCRIPTION</span></span>
<span data-ttu-id="f4a1e-109">**新的-AzureRmApplicationGatewayRedirectConfiguration** Cmdlet 會為應用程式閘道建立重新導向配置。</span><span class="sxs-lookup"><span data-stu-id="f4a1e-109">**The New-AzureRmApplicationGatewayRedirectConfiguration** cmdlet creates a redirect configuration for an application gateway.</span></span>

## <span data-ttu-id="f4a1e-110">示例</span><span class="sxs-lookup"><span data-stu-id="f4a1e-110">EXAMPLES</span></span>

### <span data-ttu-id="f4a1e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f4a1e-111">Example 1</span></span>
```
PS C:\>$RedirectConfig = New-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -RedirectType Permanent -TargetListener $listener01
```

<span data-ttu-id="f4a1e-112">這個命令會建立名為 Redirect01 的重新導向配置，並將結果儲存在名為 $RedirectConfig 的變數中。</span><span class="sxs-lookup"><span data-stu-id="f4a1e-112">This command creates a redirect configuration named Redirect01 and stores the result in the variable named $RedirectConfig.</span></span>

## <span data-ttu-id="f4a1e-113">參數</span><span class="sxs-lookup"><span data-stu-id="f4a1e-113">PARAMETERS</span></span>

### <span data-ttu-id="f4a1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a1e-114">-DefaultProfile</span></span>
<span data-ttu-id="f4a1e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4a1e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4a1e-116">-IncludePath</span><span class="sxs-lookup"><span data-stu-id="f4a1e-116">-IncludePath</span></span>
<span data-ttu-id="f4a1e-117">在重新導向的 url 中包含路徑。</span><span class="sxs-lookup"><span data-stu-id="f4a1e-117">Include path in the redirected url.</span></span>
<span data-ttu-id="f4a1e-118">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="f4a1e-118">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a1e-119">-IncludeQueryString</span><span class="sxs-lookup"><span data-stu-id="f4a1e-119">-IncludeQueryString</span></span>
<span data-ttu-id="f4a1e-120">在重新導向的 url 中包含查詢字串。</span><span class="sxs-lookup"><span data-stu-id="f4a1e-120">Include query string in the redirected url.</span></span>
<span data-ttu-id="f4a1e-121">預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="f4a1e-121">Default is true.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a1e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4a1e-122">-Name</span></span>
<span data-ttu-id="f4a1e-123">重新導向配置的名稱</span><span class="sxs-lookup"><span data-stu-id="f4a1e-123">The name of the Redirect Configuration</span></span>

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

### <span data-ttu-id="f4a1e-124">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="f4a1e-124">-RedirectType</span></span>
<span data-ttu-id="f4a1e-125">重新導向的類型</span><span class="sxs-lookup"><span data-stu-id="f4a1e-125">The type of redirect</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Permanent, Found, SeeOther, Temporary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a1e-126">-TargetListener</span><span class="sxs-lookup"><span data-stu-id="f4a1e-126">-TargetListener</span></span>
<span data-ttu-id="f4a1e-127">HTTPListener 以將要求重新導向至</span><span class="sxs-lookup"><span data-stu-id="f4a1e-127">HTTPListener to redirect the request to</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a1e-128">-TargetListenerID</span><span class="sxs-lookup"><span data-stu-id="f4a1e-128">-TargetListenerID</span></span>
<span data-ttu-id="f4a1e-129">要重新導向要求的偵聽程式識別碼</span><span class="sxs-lookup"><span data-stu-id="f4a1e-129">ID of  listener to redirect the request to</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a1e-130">-TargetUrl</span><span class="sxs-lookup"><span data-stu-id="f4a1e-130">-TargetUrl</span></span>
<span data-ttu-id="f4a1e-131">目標 URL fo</span><span class="sxs-lookup"><span data-stu-id="f4a1e-131">Target URL fo redirection</span></span>

```yaml
Type: String
Parameter Sets: SetByURL
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a1e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a1e-132">CommonParameters</span></span>
<span data-ttu-id="f4a1e-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4a1e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a1e-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4a1e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a1e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f4a1e-135">INPUTS</span></span>

### <span data-ttu-id="f4a1e-136">所有</span><span class="sxs-lookup"><span data-stu-id="f4a1e-136">None</span></span>

## <span data-ttu-id="f4a1e-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f4a1e-137">OUTPUTS</span></span>

### <span data-ttu-id="f4a1e-138">PSApplicationGatewayRedirectConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f4a1e-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="f4a1e-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f4a1e-139">NOTES</span></span>

## <span data-ttu-id="f4a1e-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4a1e-140">RELATED LINKS</span></span>

